# Lab 1: JAN MUCHA

### De Morgan's laws

1. Equations of all three versions of logic function f(c,b,a):

   ![screenshot2](https://user-images.githubusercontent.com/99410528/154537807-4e1b20f7-0d22-4b01-b1c3-5dcc87fe7a91.png)

2. Listing of VHDL architecture from design file (`design.vhd`) for all three functions. Always use syntax highlighting, meaningful comments, and follow VHDL guidelines:

```vhdl
architecture dataflow of demorgan is
begin
    forg_o  <= (not b_i and a_i) or (not c_i and not b_i);
    fnand_o <= ((a_i nand (b_i nand b_i)) nand ((b_i nand b_i) nand (c_i nand c_i)));
    fnor_o  <= (b_i nor (a_i nor (c_i nor c_i)));
end architecture dataflow;
```

3. Complete table with logic functions' values:

| **c** | **b** |**a** | **f(c,b,a)** | **f_NAND(c,b,a)** | **f_NOR(c,b,a)** |
| :-: | :-: | :-: | :-: | :-: | :-: |
| 0 | 0 | 0 | 1 | 1 | 1 |
| 0 | 0 | 1 | 1 | 1 | 1 |
| 0 | 1 | 0 | 0 | 0 | 0 |
| 0 | 1 | 1 | 0 | 0 | 0 |
| 1 | 0 | 0 | 0 | 0 | 0 |
| 1 | 0 | 1 | 1 | 1 | 1 |
| 1 | 1 | 0 | 0 | 0 | 0 |
| 1 | 1 | 1 | 0 | 0 | 0 |

### Distributive laws

1. Screenshot with simulated time waveforms. Always display all inputs and outputs (display the inputs at the top of the image, the outputs below them) at the appropriate time scale!

   ![screenshot1](https://user-images.githubusercontent.com/99410528/154537588-9dd63651-965f-4fc8-a7a4-5943d0dfc0cf.png)

2. Link to your public EDA Playground example:

   https://www.edaplayground.com/x/CxPU
