# Portfolio-Overlap-Analysis
This program is designed to calculate the overlap between different funds based on the stocks they hold and their respective weights.
The input file is in excel format and has the following columns - Scheme Name, Company Name, ISIN, Sector Name, % of Net Assets.
The overlap can be caluclated either basis the company name or basis the ISIN. The program has the code for both the options.
Overlap is caluclated as follows - the program takes the common stocks between two funds and sums the minimum weight of the stocks.
The detailed working of the program is given below:

1. The program defines a function named `overlap` that takes two fund names (`fund1` and `fund2`) as input and calculates the overlap between the stocks held by the two funds.
2. The function extracts the stocks held by `fund1` and `fund2` from a DataFrame `df` based on the 'Scheme Name' column.
3. It identifies the common stocks held by both funds by taking the intersection of the stocks.
4. The function iterates over each common stock and calculates the overlap by considering the weights of the stock in `fund1` and `fund2`. It adds the smaller weight to the overlap sum.
5. The function returns the calculated overlap sum.
6. The program defines another function named `overlap_table_comp` that takes a list of fund names (`funds2`) as input and generates an overlap table for the given funds.
7. The function initializes a DataFrame named `table_comp` filled with zeros, with rows and columns corresponding to the funds in the `funds2` list.
8. The function calculates the overlap between each pair of funds in `funds2` by calling the `overlap` function. The resulting overlap values are stored in the appropriate cells of the `table_comp` DataFrame.
9. The function returns the generated overlap table.
10. The program provides an example usage where it defines a list of fund names (`funds2`) and calls the `overlap_table_comp` function with `funds2` as input. The resulting overlap table is stored in the `table_comp` variable and then displayed.
