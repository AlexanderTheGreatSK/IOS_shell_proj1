# IOS_shell_proj1

Shell project for sorting, filtering and data processing for given tradelog file.
Drawing graph is also supported.

Examples of `.log` files are included in repository.

## Usage

`tradelog [-h|--help]`


`tradelog [FILTER ...] [COMMAND] [LOG [LOG2 [...]]`
  
- `COMMAND`
  - `list-tick`       prints list of occurring stock symbols (tickers)
  - `profit`          prints total profit from closed positions
  - `pos`             prints list of values of currently held positions sorted in descending order by value
  - `last-price`      prints list of the last known price for each ticker
  - `hist-ord`        prints histogram of the number of transactions according to the ticker
  - `graph-pos`       prints graph of values of held positions according to the ticker

- `FILTER`
  - `-a DATETIME`     considered are only values of records after this date (without this date) `DATETIME` is in format `YYYY-MM-DD HH:MM:SS`
  - `-b DATETIME`     considered are only values of records before this date (without this date) `DATETIME` is in format `YYYY-MM-DD HH:MM:SS`
  - `-t TICKER`       considered are only entries corresponding to a given ticker. With multiple occurrences of this switch, the set of all listed                               tickers are taken
  - `-w WIDTH`        sets width of graph, specified value sets length of the longest line. `WIDTH` must be unsigned integer
                        Multiple occurrences of this switch are not allowed, program will end with error
