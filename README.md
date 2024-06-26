# gbtul
Notes and models for using https://sites.fct.unl.pt/gbt/

# Notes

## Units
As default kN, mm, s

## Decimal separator
To input decimal numbers, separator for active locale must be used. E.g. for fi , is used although . is used in outputs.

## UI GBTUL.exe
Written in C# and uses dotnet 4 https://dotnet.microsoft.com/en-us/download/dotnet-framework/net48

## Solver GBT.exe
Written in fortran-90. Many input file names and print templates are shown using process explorer's Strings tab.
Image is 32-bit.
Input and output filenames are available in GBTUL.exe.config

Used files are studied below. Sample files are for imaginary rhs-100x100x4 with sharp corners 
### Input-Files
#### UNIT 1  - inp1.txt
comment after --
```
4 -- number of nodes
0   0 -- coordinates
100   0
100   100
0   100
4 -- elements
1  2  1  0  4 -- i-node j-node material intermediate-nodes thickness
2  3  1  0  4
3  4  1  0  4
4  1  1  0  4
1 -- Materials
210000  210000  0.3  0.3  80769.2307692308  7.8E-06 - Exx Ess nu-xs nu-sx G rho
0 -- Length-Distributed Elastic Supports and Additional Masses
0 -- Distributed along longitudinal strips 
```
Reflects UI's Cross-Section Analysis tab
![image](https://github.com/simo-11/gbtul/assets/1210784/ddee0705-6619-4e9c-823b-2b30b19c292e)

#### UNIT 2 - inp2.txt

```
1 0 1 1
```

#### UNIT 3 - inp3.txt

```
1 0
1
3
64 -- number of lengths
10
..
10000
1 0 0 0
10 10
```

#### Unit 135 - inp4.txt
```
2
33
1
0
1
2
1
```

### Output-Files

#### out1.txt Cross-Section Geometrical Properties
```
     1600.000000000000000
  2667733.333333339000000  2667733.333333333000000
  1777777.777777777000000  4008533.333333334000000
       50.000000000000000       50.000000000000000
       50.000000000000000       50.000000000000000
   0.000000000000000E+000   0.000000000000000E+000

```
Shown in UI Mode selection tab
![image](https://github.com/simo-11/gbtul/assets/1210784/b94c51b5-361c-4192-b3ac-1175be8f15de)


#### out2.txt

#### out3.txt

#### out4.txt

#### out5.txt


#### Output_Files/GBT_Modes.csv

#### Output_Files/Mafuncs.csv

#### Output_Files/Matrices.csv

#### Output_Files/Results.csv


