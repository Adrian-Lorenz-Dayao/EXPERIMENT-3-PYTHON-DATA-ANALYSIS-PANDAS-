# EXPERIMENT-3-PYTHON-DATA-ANALYSIS-PANDAS

**Made by: Adrian Lorenz I. Dayao | 2ECE-A**

The objectives of the experiment will be to successfully utilize the pandas python library to manipulate and process data from a csv file through the utilization of dataframes. A sammple file cars.csv will be used as the basis for the dataframe values and will be imported into the programs with variable name `cars` 

# **A. POSITIONAL AND LABEL-BASED SLICING**

a.) This first part of the program displays the read csv file saved in the cars variable as a dataframe using `pd.read_csv('cars.csv')`, with expected output of:

|    | Model               |   mpg |   cyl |   disp |   hp |   drat |    wt |   qsec |   vs |   am |   gear |   carb |
|---:|:--------------------|------:|------:|-------:|-----:|-------:|------:|-------:|-----:|-----:|-------:|-------:|
|  0 | Mazda RX4           |  21   |     6 |  160   |  110 |   3.9  | 2.62  |  16.46 |    0 |    1 |      4 |      4 |
|  1 | Mazda RX4 Wag       |  21   |     6 |  160   |  110 |   3.9  | 2.875 |  17.02 |    0 |    1 |      4 |      4 |
|  2 | Datsun 710          |  22.8 |     4 |  108   |   93 |   3.85 | 2.32  |  18.61 |    1 |    1 |      4 |      1 |
|  3 | Hornet 4 Drive      |  21.4 |     6 |  258   |  110 |   3.08 | 3.215 |  19.44 |    1 |    0 |      3 |      1 |
|  4 | Hornet Sportabout   |  18.7 |     8 |  360   |  175 |   3.15 | 3.44  |  17.02 |    0 |    0 |      3 |      2 |
|  5 | Valiant             |  18.1 |     6 |  225   |  105 |   2.76 | 3.46  |  20.22 |    1 |    0 |      3 |      1 |
|  6 | Duster 360          |  14.3 |     8 |  360   |  245 |   3.21 | 3.57  |  15.84 |    0 |    0 |      3 |      4 |
|  7 | Merc 240D           |  24.4 |     4 |  146.7 |   62 |   3.69 | 3.19  |  20    |    1 |    0 |      4 |      2 |
|  8 | Merc 230            |  22.8 |     4 |  140.8 |   95 |   3.92 | 3.15  |  22.9  |    1 |    0 |      4 |      2 |
|  9 | Merc 280            |  19.2 |     6 |  167.6 |  123 |   3.92 | 3.44  |  18.3  |    1 |    0 |      4 |      4 |
| 10 | Merc 280C           |  17.8 |     6 |  167.6 |  123 |   3.92 | 3.44  |  18.9  |    1 |    0 |      4 |      4 |
| 11 | Merc 450SE          |  16.4 |     8 |  275.8 |  180 |   3.07 | 4.07  |  17.4  |    0 |    0 |      3 |      3 |
| 12 | Merc 450SL          |  17.3 |     8 |  275.8 |  180 |   3.07 | 3.73  |  17.6  |    0 |    0 |      3 |      3 |
| 13 | Merc 450SLC         |  15.2 |     8 |  275.8 |  180 |   3.07 | 3.78  |  18    |    0 |    0 |      3 |      3 |
| 14 | Cadillac Fleetwood  |  10.4 |     8 |  472   |  205 |   2.93 | 5.25  |  17.98 |    0 |    0 |      3 |      4 |
| 15 | Lincoln Continental |  10.4 |     8 |  460   |  215 |   3    | 5.424 |  17.82 |    0 |    0 |      3 |      4 |
| 16 | Chrysler Imperial   |  14.7 |     8 |  440   |  230 |   3.23 | 5.345 |  17.42 |    0 |    0 |      3 |      4 |
| 17 | Fiat 128            |  32.4 |     4 |   78.7 |   66 |   4.08 | 2.2   |  19.47 |    1 |    1 |      4 |      1 |
| 18 | Honda Civic         |  30.4 |     4 |   75.7 |   52 |   4.93 | 1.615 |  18.52 |    1 |    1 |      4 |      2 |
| 19 | Toyota Corolla      |  33.9 |     4 |   71.1 |   65 |   4.22 | 1.835 |  19.9  |    1 |    1 |      4 |      1 |
| 20 | Toyota Corona       |  21.5 |     4 |  120.1 |   97 |   3.7  | 2.465 |  20.01 |    1 |    0 |      3 |      1 |
| 21 | Dodge Challenger    |  15.5 |     8 |  318   |  150 |   2.76 | 3.52  |  16.87 |    0 |    0 |      3 |      2 |
| 22 | AMC Javelin         |  15.2 |     8 |  304   |  150 |   3.15 | 3.435 |  17.3  |    0 |    0 |      3 |      2 |
| 23 | Camaro Z28          |  13.3 |     8 |  350   |  245 |   3.73 | 3.84  |  15.41 |    0 |    0 |      3 |      4 |
| 24 | Pontiac Firebird    |  19.2 |     8 |  400   |  175 |   3.08 | 3.845 |  17.05 |    0 |    0 |      3 |      2 |
| 25 | Fiat X1-9           |  27.3 |     4 |   79   |   66 |   4.08 | 1.935 |  18.9  |    1 |    1 |      4 |      1 |
| 26 | Porsche 914-2       |  26   |     4 |  120.3 |   91 |   4.43 | 2.14  |  16.7  |    0 |    1 |      5 |      2 |
| 27 | Lotus Europa        |  30.4 |     4 |   95.1 |  113 |   3.77 | 1.513 |  16.9  |    1 |    1 |      5 |      2 |
| 28 | Ford Pantera L      |  15.8 |     8 |  351   |  264 |   4.22 | 3.17  |  14.5  |    0 |    1 |      5 |      4 |
| 29 | Ferrari Dino        |  19.7 |     6 |  145   |  175 |   3.62 | 2.77  |  15.5  |    0 |    1 |      5 |      6 |
| 30 | Maserati Bora       |  15   |     8 |  301   |  335 |   3.54 | 3.57  |  14.6  |    0 |    1 |      5 |      8 |
| 31 | Volvo 142E          |  21.4 |     4 |  121   |  109 |   4.11 | 2.78  |  18.6  |    1 |    1 |      4 |      2 |

b.) The 2nd part for program A extracts rows of index 6- using the .iloc function into a new dataframe (with variable name b1) whose row index is reset and begins at 1. Expected output is therefore:

|    | Model      |   mpg |   cyl |   disp |   hp |   drat |   wt |   qsec |   vs |   am |   gear |   carb |
|---:|:-----------|------:|------:|-------:|-----:|-------:|-----:|-------:|-----:|-----:|-------:|-------:|
|  1 | Duster 360 |  14.3 |     8 |  360   |  245 |   3.21 | 3.57 |  15.84 |    0 |    0 |      3 |      4 |
|  2 | Merc 240D  |  24.4 |     4 |  146.7 |   62 |   3.69 | 3.19 |  20    |    1 |    0 |      4 |      2 |
|  3 | Merc 230   |  22.8 |     4 |  140.8 |   95 |   3.92 | 3.15 |  22.9  |    1 |    0 |      4 |      2 |
|  4 | Merc 280   |  19.2 |     6 |  167.6 |  123 |   3.92 | 3.44 |  18.3  |    1 |    0 |      4 |      4 |
|  5 | Merc 280C  |  17.8 |     6 |  167.6 |  123 |   3.92 | 3.44 |  18.9  |    1 |    0 |      4 |      4 |

```python
b1 = cars.iloc[[6,7,8,9,10]] #saves the rows with indexes 6-10 from cars dataframe
b1 = b1.reset_index(drop=True) #resets the index of b1
b1.index = b1.index + 1 #starts b1 index at 1

b1 #output
```
c.) The final part of program A takes the saved dataframe b1 from letter b. and saves only columns Model, mpg, cyl, hp, and gear, in that order through the use of column labels with the .loc function. Expected output is therefore:

|    | Model      |   mpg |   cyl |   hp |   gear |
|---:|:-----------|------:|------:|-----:|-------:|
|  1 | Duster 360 |  14.3 |     8 |  245 |      3 |
|  2 | Merc 240D  |  24.4 |     4 |   62 |      4 |
|  3 | Merc 230   |  22.8 |     4 |   95 |      4 |
|  4 | Merc 280   |  19.2 |     6 |  123 |      4 |
|  5 | Merc 280C  |  17.8 |     6 |  123 |      4 |

```python
bx = b1.loc[:, ['Model', 'mpg', 'cyl', 'hp', 'gear']]#shows only chosen columns from b1
print(bx)
```

# **B. MODEL LOOKUP**

Program B extracts certain rows from the cars dataframe through the use of boolean indexing. The following program makes use of the `==` conditional on the Model coloumn inorder to exclusively filter specific dataframe rows.

a.) The first half for program B extracts any row with model Toyota Corolla and saves it as variable toyota. It therefore has expected output:

|    | Model          |   mpg |   cyl |   disp |   hp |   drat |    wt |   qsec |   vs |   am |   gear |   carb |
|---:|:---------------|------:|------:|-------:|-----:|-------:|------:|-------:|-----:|-----:|-------:|-------:|
| 19 | Toyota Corolla |  33.9 |     4 |   71.1 |   65 |   4.22 | 1.835 |   19.9 |    1 |    1 |      4 |      1 |

```python
toyota = cars[(cars['Model']=='Toyota Corolla')] #saves any Toyota Corolla row from cars dataframe
print(toyota)
```
b.) The second half of program B extracts any row with model Pontiac Firebird and saves it as variable pontiac while only displaying columns for Model, mpg, hp, and wt. It therefore has expected output:

|    | Model            |   mpg |   hp |    wt |
|---:|:-----------------|------:|-----:|------:|
| 24 | Pontiac Firebird |  19.2 |  175 | 3.845 |

```python
pontiac1 = cars[(cars['Model']=='Pontiac Firebird')] #saves any Pontiac Firebird row from cars dataframe
pontiac = pontiac1.loc[:, ['Model','mpg','hp','wt']] #only shows chosen columns from saved pontiac row dataframe
print(pontiac)
```

# **C. MULTI-MODEL SUBSETTING**

Program C creates a dataFrame saved as variable selected cars containing only the records for models Datsun 710, Lotus Europa, and Ferrari Dino; where only retained columns are Model, mpg, cyl, hp, and gear with the restriction being that the rows are selected by their model values. It therefore has expected output:

|    | Model        |   mpg |   cyl |   hp |   gear |
|---:|:-------------|------:|------:|-----:|-------:|
|  2 | Datsun 710   |  22.8 |     4 |   93 |      4 |
| 27 | Lotus Europa |  30.4 |     4 |  113 |      5 |
| 29 | Ferrari Dino |  19.7 |     6 |  175 |      5 |

```python
datsun = cars[(cars['Model']=='Datsun 710')]
lotus = cars[(cars['Model']=='Lotus Europa')]
ferrari = cars[(cars['Model']=='Ferrari Dino')] #individually saves chosen car models to their own respective dataframe rows

selected_cars = pd.concat([datsun, lotus, ferrari]) #stacks the car model rows into 1 dataframe saved as selected_cars
selected_cars = selected_cars.loc[:, ['Model','mpg','cyl','hp','gear']] #only shows chosen columns of stacked dataframe selected

print(selected_cars)
```