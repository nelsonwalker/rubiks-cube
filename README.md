# Rubik's Cube Solver

Solves a Rubik's cube in C

## Testing

Prerequisites:
  - gcc compiler

1. go to https://iamthecu.be/ 
2. click shuffle until it is appropriately shuffled
3. using the labels function, make sure the "front" face is white, the "right" face is <span style="color:green">green</span>, and the "up" face is <span style="color:red">red</span>
4. navigate to your text editor, create a text file, `test-input.txt`, and copy the state of the cube into it. The text file will look like:

<span style="color:yellow">xxxxyxxxx</span><span style="color:white">xxxxwxxxx</span><span style="color:blue">xxxxbxxxx</span><span style="color:orange">xxxxoxxxx</span><span style="color:green">xxxxgxxxx</span><span style="color:red">xxxxrxxxx</span>

where:
  - <span style="color:yellow">xxxxyxxxx</span> is all the squares of the yellow face (side with yellow in the middle square) listed from left to right, top to bottom. When reading the squares, the cube should be oriented such that the <span style="color:green">green</span> side is at the top of the cube
  - <span style="color:white">xxxxwxxxx</span> same as above but for white, and the <span style="color:blue">blue</span> side is at the top of the cube
  - <span style="color:blue">xxxxbxxxx</span> same as above but for blue, and the <span style="color:yellow">yellow</span> side is at the top of the cube
  - <span style="color:orange">xxxxoxxxx</span> is same as above but for orange, and the <span style="color:yellow">yellow</span> side is at the top of the cube
  - <span style="color:green">xxxxgxxxx</span> is same as above but for green, and the <span style="color:yellow">yellow</span> side is at the top of the cube
  - <span style="color:red">xxxxrxxxx</span> is same as above but for red, and the <span style="color:yellow">yellow</span> side is at the top of the cube
  - here 'x' is just a placeholder for one of (<span style="color:yellow">y</span>, <span style="color:white">w</span>, <span style="color:blue">b</span>, <span style="color:orange">o</span>, <span style="color:green">g</span>, <span style="color:red">r</span>) 
5. build the solver executable:
```bash
make solver
```
6. run the program:
```bash
./solver < test-input.txt
```
7. the output will look something like this:
```
RBDBBBUUULLBBDDBBBRRUUBBDDDBBBDUUUBUDBBBDDDRBRRRBBLLLBBBLRRRBRDBDDD...
```
copy this string, open the console on the Rubik's cube website, and type:
```js
cube.twist('RBDBBBUUULLBBDDBBBRRUUBBDDDBBBDUUUBUDBBBDDDRBRRRBBLLLBBBLRRRBRDBDDD...')
```

now watch the Rubik's cube get solved.

## Demo
