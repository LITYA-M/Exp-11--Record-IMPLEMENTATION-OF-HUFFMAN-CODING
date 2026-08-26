# Exp-11--Record-IMPLEMENTATION-OF-HUFFMAN-CODING
# Aim
To implement Huffman coding to compress the data using Python.

# Software Required

. Anaconda - Python 3.7

# Algorithm:
## Step1:
Get the input string

## Step2:
Calculate frequency of each character in the input string

## Step3:
Create tree nodes

## Step4:
Main function to implement Huffman coding

## Step5:
Generate Huffman codes

## Step6:
Print the characters and their Huffman codes

# Program:

Name : LITYA M

Reg.no: 212225230152

Get the input String
```
input_string = "FRIENDS_FOREVER"
```
Calculate frequency of each character in the input string

```
frequency = {}
for char in input_string:
    if char in frequency:
        frequency[char] += 1
    else:
        frequency[char] = 1
```

Create tree nodes
```
nodes = [[char, freq] for char, freq in frequency.items()]
```
Main function to implement Huffman coding
```
while len(nodes) > 1:
    # Sort nodes based on frequency
    nodes = sorted(nodes, key=lambda x: x[1])

    # Pick two smallest nodes
    left = nodes.pop(0)
    right = nodes.pop(0)

    # Create a new node with combined frequency
    new_node = [[left, right], left[1] + right[1]]
    nodes.append(new_node)

# The final node is the Huffman tree
huffman_tree = nodes[0]
```
Generate Huffman codes
```
huffman_codes = {}

def generate_codes(tree, code=""):
    if isinstance(tree[0], str):  # If it's a leaf node
        huffman_codes[tree[0]] = code
    else:  # If it's an internal node, recurse
        generate_codes(tree[0][0], code + "0")
        generate_codes(tree[0][1], code + "1")

generate_codes(huffman_tree)
```
 Print the characters and their Huffman codes
 ```
print("Character | Huffman Code")
print("-------------------------")
for char, code in huffman_codes.items():
    print(f"    {char}    |    {code}")
```
# Output:
<img width="267" height="270" alt="image" src="https://github.com/user-attachments/assets/36d9260a-546a-4c37-8169-de125e8820ff" />


# Result:
Thus the huffman coding was implemented to compress the data using python programming.













..
















..













..








...













..












..












..
















..











..











..













..













...










..











..











..














..








..








...











...










..












....












...











....



















..
