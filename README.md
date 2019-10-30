# PageRank Algorithm

A Java implementation of the PageRank algorithm, run on the CiteSeer citation graph.

This is **Project 0** for **ITCS414 Information Storage and Retrieval** at the Faculty of ICT, Mahidol University (MUICT).

## What it does

`PageRanker` reads a directed graph, gives each page a PageRank score by iterating until the scores stop changing much, and then prints the top 100 pages.

- **Input:** `citeseer.dat`. Each line is `<pid_1> <pid_2> ... <pid_n>`, where pages `pid_2 … pid_n` link to (cite) page `pid_1`.
- **Damping factor:** `d = 0.85`
- **Stopping rule:** the ones digit of the perplexity stays the same for 3 iterations in a row.
- **Sink pages** (pages with no out-links) share their rank evenly across all pages.

### Output

| File | Contents |
| --- | --- |
| `perplexity.out` | Perplexity after each iteration, one value per line |
| `pr_scores.out` | `<page_id> <score>` for every page |
| stdout | Top 100 page IDs and the processing time |

## How to run

Requires JDK 8 or newer.

1. Put the dataset `citeseer.dat` in the project root. It is not included in this repository.
2. Compile and run:

   ```bash
   javac PageRanker.java
   java PageRanker
   ```

   In IntelliJ IDEA, open the folder and run `PageRanker.main`. Make sure the working directory is the project root.

3. Results are written to `perplexity.out` and `pr_scores.out`. These files are overwritten on every run.

## Authors

- Klinton
- Fha
- Ploy
