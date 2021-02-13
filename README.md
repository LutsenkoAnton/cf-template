# cf-template
This is a template for C++ olympiad program. I prefer using [cf-tool](https://github.com/xalanq/cf-tool) when generating template for my programs.

All your code should be written in function ```solve()``` (not ```main()```)

## Template Settings
On line 13 you can find Settings. Uncomment setting that you would like to change
| Setting | Changes |
| --- | --- |
| UNORDERED | Changes ```set``` and ```map``` to ```unordered_set``` and ```unordered_map``` respectively |
| FILE | Uncomment to switch to file input. If necessary, change default names for input and output files on lines 23 and 24 |
| MANYTIMES | Necessary when one test consits of several test cases |
| ```#define int long long``` | Changes int type to long long, so you don't need to worry about integer overflow |
| UPPER | Changes ```"Yes"``` and ```"No"``` to ```"YES"``` and ```"NO"``` respectively (see ```yes()``` and ```no()``` functions description for more information)
| LOWER | Changes ```"Yes"``` and ```"No"``` to ```"yes"``` and ```"no"``` respectively (see ```yes()``` and ```no()``` functions description for more information)

On lines 21-24 you can change some constants:
| Constant | Purpose |
| --- | --- |
| MAXN | Size of array. Usually it is upper bound for size of input arrays. |
| MOD | Necessary for modular arithmetic. Usually it is a big prime number |
| filein | Name of input file (see FILE setting) |
| fileout | Name of output file (see FILE setting) |

## Shortcuts
### Type shortcuts
| Shortcut | Meaning |
| --- | --- |
|``` vint``` | ```vector<int>``` |
| ```aint ```| ```array<int, MAXN>``` |
| ```adouble```| ```array<double, MAXN>``` |
|``` mint``` | ```map<int, int>``` |
|``` gr``` | ```array<vector<int>, MAXN>``` (usually used for graphs) |
|``` pint``` | ```pait<int, int>``` |
### Cycle shortcuts
| Shortcut | Meaning |
| --- | --- |
| ```REP(i)``` | Iterates i from 0 to n |
| ```REP1(i, e)``` | Iterates i from 0 to e |
| ```REP2(i, e)``` | Iterates i from b to e |
| ```REP3(e, s)``` | Iterates e over structure s |
### Other shortcuts
| Shortcut | Meaning |
| --- | --- |
| ```ft``` | ```first```  |
|``` sd``` | ```second```  |
| ```all(s)``` | ```s.begin(), s.end()```  (useful for STL algorithms with vectors) |
| ```all2(s, n)``` | ```s.begin(), s.begin() + n```  (useful for STL algorithms eith arrays) |
| ```pb``` | ```push_back``` |
| ```mp``` | ```make_pair``` |
| ```mt``` | ```make_tuple``` |
| ```lb``` | ```lower_bound``` |
| ```ub``` | ```upper_bound``` |
| ```ins``` | ```insert``` |

## Functions
Support for inputing and printing vectors and pairs with ```cin >> ``` and ``` cout << ```
Added function ```input(a, n)``` to input an array of ```n``` elements
Function ```print(a, n, sep)``` can print array or vector of ```n``` elements with separator ```sep``` (space by default)
Fucntions ```yes(ret)``` and ```no(ret)``` help to print result of the program. If ```ret``` is 1 the program will stop immediately else it just prints ```"Yes"``` or ```"No"```. The functions are customized with ```UPPER``` and ```LOWER``` settings (see "Settings"). By default output is capitalized. UPPER setting changes output to uppercased and LOWER changes output to lowercased. UPPER has higher priority than LOWER.
