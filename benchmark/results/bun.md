# Bun

## structuredClone

|            | hasTransferables       | structuredClone (no transfer) | structuredClone (manually) | structuredClone (manually) (transfer) | structuredClone (getTransferables) | structuredClone (getTransferables) (transfer) | structuredClone (getTransferable*) | structuredClone (getTransferable*) (transfer) |
| ---------- | ---------------------- | ----------------------------- | -------------------------- | ------------------------------------- | ---------------------------------- | --------------------------------------------- | ---------------------------------- | --------------------------------------------- |
| 1 B        | in 0.205 ms ± 0.251 ms | null                          | in 0.055 ms ± 0.026 ms     | in 7.978 ms ± 2.236 ms                | in 0.288 ms ± 0.203 ms             | in 7.343 ms ± 0.858 ms                        | in 0.367 ms ± 0.303 ms             | in 7.239 ms ± 1.117 ms                        |
| 2 B        | in 0.074 ms ± 0.011 ms | null                          | in 0.037 ms ± 0.008 ms     | in 6.615 ms ± 0.894 ms                | in 0.222 ms ± 0.11 ms              | in 7.189 ms ± 1.187 ms                        | in 0.259 ms ± 0.125 ms             | in 7.278 ms ± 1.38 ms                         |
| 4 B        | in 0.079 ms ± 0.019 ms | null                          | in 0.037 ms ± 0.01 ms      | in 6.924 ms ± 1.62 ms                 | in 0.219 ms ± 0.067 ms             | in 7.789 ms ± 3.057 ms                        | in 0.268 ms ± 0.092 ms             | in 8.067 ms ± 1.801 ms                        |
| 8 B        | in 0.1 ms ± 0.033 ms   | null                          | in 0.04 ms ± 0.012 ms      | in 6.755 ms ± 0.773 ms                | in 0.233 ms ± 0.118 ms             | in 8.655 ms ± 4.587 ms                        | in 0.246 ms ± 0.041 ms             | in 6.826 ms ± 1.366 ms                        |
| 16 B       | in 0.062 ms ± 0.015 ms | null                          | in 0.043 ms ± 0.026 ms     | in 6.319 ms ± 0.395 ms                | in 0.166 ms ± 0.013 ms             | in 24.923 ms ± 9.803 ms                       | in 0.216 ms ± 0.011 ms             | in 6.752 ms ± 0.961 ms                        |
| 32 B       | in 0.075 ms ± 0.033 ms | null                          | in 0.045 ms ± 0.031 ms     | in 6.245 ms ± 0.611 ms                | in 0.179 ms ± now                  | in 6.098 ms ± 0.65 ms                         | in 0.217 ms ± 0.009 ms             | in 6.146 ms ± 0.661 ms                        |
| 64 B       | in 0.056 ms ± now      | null                          | in 0.03 ms ± 0.007 ms      | in 6.005 ms ± 0.531 ms                | in 0.215 ms ± 0.019 ms             | in 6.206 ms ± 0.525 ms                        | in 0.254 ms ± 0.047 ms             | in 6.156 ms ± 0.233 ms                        |
| 128 B      | in 0.054 ms ± now      | null                          | in 0.03 ms ± 0.008 ms      | in 5.865 ms ± 0.296 ms                | in 0.275 ms ± 0.02 ms              | in 6.835 ms ± 0.964 ms                        | in 0.307 ms ± 0.013 ms             | in 9.111 ms ± 5.797 ms                        |
| 256 B      | in 0.064 ms ± 0.022 ms | null                          | in 0.026 ms ± now          | in 5.972 ms ± 0.154 ms                | in 0.674 ms ± 0.482 ms             | in 6.819 ms ± 0.636 ms                        | in 0.434 ms ± 0.03 ms              | in 7.024 ms ± 0.281 ms                        |
| 512 B      | in 0.058 ms ± 0.007 ms | null                          | in 0.026 ms ± now          | in 9.666 ms ± 4.314 ms                | in 0.626 ms ± 0.022 ms             | in 8.148 ms ± 0.582 ms                        | in 0.691 ms ± 0.059 ms             | in 9.694 ms ± 2.231 ms                        |
| 1.024 kB   | in 0.064 ms ± 0.013 ms | null                          | in 0.027 ms ± now          | in 8.717 ms ± 0.746 ms                | in 1.108 ms ± 0.073 ms             | in 9.751 ms ± 0.676 ms                        | in 1.139 ms ± 0.015 ms             | in 10.187 ms ± 1.022 ms                       |
| 2.048 kB   | in 0.073 ms ± 0.035 ms | null                          | in 0.031 ms ± 0.009 ms     | in 12.523 ms ± 1.558 ms               | in 1.988 ms ± 0.106 ms             | in 14.931 ms ± 5.075 ms                       | in 2.191 ms ± 0.202 ms             | in 13.095 ms ± 1.031 ms                       |
| 4.096 kB   | in 0.058 ms ± 0.009 ms | null                          | in 0.035 ms ± 0.01 ms      | in 15.732 ms ± 1.045 ms               | in 3.91 ms ± 0.229 ms              | in 18.532 ms ± 0.545 ms                       | in 3.879 ms ± 0.098 ms             | in 19.442 ms ± 1.212 ms                       |
| 8.192 kB   | in 0.073 ms ± 0.027 ms | null                          | in 0.03 ms ± now           | in 24.618 ms ± 1.775 ms               | in 7.49 ms ± 0.177 ms              | in 35.488 ms ± 3.85 ms                        | in 8.247 ms ± 0.929 ms             | in 32.6 ms ± 1.237 ms                         |
| 16.384 kB  | in 0.079 ms ± 0.011 ms | null                          | in 0.05 ms ± 0.01 ms       | in 48.796 ms ± 2.603 ms               | in 15.395 ms ± 0.603 ms            | in 61.174 ms ± 3.768 ms                       | in 15.993 ms ± 0.819 ms            | in 60.497 ms ± 1.418 ms                       |
| 32.768 kB  | in 0.072 ms ± 0.013 ms | null                          | in 0.04 ms ± now           | in 85.309 ms ± 2.914 ms               | in 30.468 ms ± 0.823 ms            | in 221.203 ms ± 66.691 ms                     | in 32.505 ms ± 3.454 ms            | in 124.663 ms ± 7.341 ms                      |
| 65.536 kB  | in 0.1 ms ± 0.02 ms    | null                          | in 0.055 ms ± 0.009 ms     | in 252.222 ms ± 73 ms                 | in 61.312 ms ± 2.142 ms            | in 238.943 ms ± 20.135 ms                     | in 62.835 ms ± 2.606 ms            | in 232.382 ms ± 17.368 ms                     |
| 131.072 kB | in 1.719 ms ± 3.22 ms  | null                          | in 0.077 ms ± now          | in 323.412 ms ± 3.076 ms              | in 118.826 ms ± 1.485 ms           | in 542.438 ms ± 94.846 ms                     | in 125.018 ms ± 3.825 ms           | in 540.092 ms ± 60.948 ms                     |
| 262.144 kB | in 0.128 ms ± 0.015 ms | null                          | in 0.077 ms ± 0.006 ms     | in 924.474 ms ± 127.666 ms            | in 330.26 ms ± 59.193 ms           | in 1,212.617 ms ± 126.67 ms                   | in 353.178 ms ± 62.294 ms          | in 1,280.155 ms ± 153.138 ms                  |
| 524.288 kB | in 0.164 ms ± 0.077 ms | null                          | in 0.094 ms ± 0.027 ms     | in 1,789.542 ms ± 207.732 ms          | in 497.881 ms ± 25.571 ms          | in 2,201.148 ms ± 186.866 ms                  | in 565.105 ms ± 64.275 ms          | in 2,305.156 ms ± 165.44 ms                   |
| 1.049 MB   | in 0.142 ms ± 0.039 ms | null                          | in 0.084 ms ± now          | in 3,329.31 ms ± 110.444 ms           | in 1,032.278 ms ± 75.432 ms        | in 4,285.02 ms ± 199.602 ms                   | in 1,038.826 ms ± 86.946 ms        | in 4,204.416 ms ± 146.722 ms                  |

## MessageChannel

|            | hasTransferables             | postMessage (no transfers) | postMessage (manually)       | postMessage (manually) (transfer) | postMessage (getTransferables) | postMessage (getTransferables) (transfer) | postMessage (getTransferable*) | postMessage (getTransferable*) (transfer) |
| ---------- | ---------------------------- | -------------------------- | ---------------------------- | --------------------------------- | ------------------------------ | ----------------------------------------- | ------------------------------ | ----------------------------------------- |
| 1 B        | in 16.97 ms ± 1.896 ms       | null                       | in 18.614 ms ± 8.289 ms      | in 35.848 ms ± 20.454 ms          | in 34.674 ms ± 17.354 ms       | in 24.969 ms ± 5.298 ms                   | in 28.039 ms ± 13.129 ms       | in 23.709 ms ± 4.522 ms                   |
| 2 B        | in 14.394 ms ± 2.531 ms      | null                       | in 13.762 ms ± 4.794 ms      | in 37.422 ms ± 22.099 ms          | in 29.01 ms ± 14.067 ms        | in 20.964 ms ± 3.395 ms                   | in 27.123 ms ± 9.483 ms        | in 21.614 ms ± 4.117 ms                   |
| 4 B        | in 13.331 ms ± 2.305 ms      | null                       | in 13.651 ms ± 4.268 ms      | in 38.169 ms ± 21.03 ms           | in 26.949 ms ± 13.828 ms       | in 20.15 ms ± 3.964 ms                    | in 34.026 ms ± 15.713 ms       | in 22.759 ms ± 4.157 ms                   |
| 8 B        | in 13.358 ms ± 2.498 ms      | null                       | in 12.693 ms ± 4.325 ms      | in 29.76 ms ± 13.169 ms           | in 28.209 ms ± 14.779 ms       | in 20.861 ms ± 3.622 ms                   | in 26.594 ms ± 13.002 ms       | in 22.185 ms ± 4.606 ms                   |
| 16 B       | in 15.658 ms ± 4.672 ms      | null                       | in 10.596 ms ± 2.958 ms      | in 26.024 ms ± 10.716 ms          | in 21.676 ms ± 13.214 ms       | in 20.622 ms ± 4.431 ms                   | in 20.785 ms ± 13.004 ms       | in 21.769 ms ± 4.258 ms                   |
| 32 B       | in 19.804 ms ± 11.057 ms     | null                       | in 10.586 ms ± 2.849 ms      | in 22.924 ms ± 5.642 ms           | in 15.828 ms ± 6.166 ms        | in 20.485 ms ± 4.575 ms                   | in 24.15 ms ± 15.159 ms        | in 21.454 ms ± 4.325 ms                   |
| 64 B       | in 21.106 ms ± 11.238 ms     | null                       | in 10.909 ms ± 2.695 ms      | in 38.18 ms ± 6.272 ms            | in 15.755 ms ± 5.452 ms        | in 36.634 ms ± 6.11 ms                    | in 14.345 ms ± 3.776 ms        | in 38.863 ms ± 6.088 ms                   |
| 128 B      | in 22.244 ms ± 16.424 ms     | null                       | in 12.579 ms ± 5.821 ms      | in 23.143 ms ± 3.747 ms           | in 13.909 ms ± 5.555 ms        | in 23.717 ms ± 4.189 ms                   | in 14.175 ms ± 3.531 ms        | in 25.222 ms ± 5.877 ms                   |
| 256 B      | in 14.839 ms ± 3.425 ms      | null                       | in 12.881 ms ± 5.004 ms      | in 29.156 ms ± 7.252 ms           | in 14.714 ms ± 5.581 ms        | in 21.954 ms ± 4.034 ms                   | in 14.634 ms ± 3.814 ms        | in 23.936 ms ± 4.977 ms                   |
| 512 B      | in 25.127 ms ± 6.255 ms      | null                       | in 27.303 ms ± 4.673 ms      | in 40.777 ms ± 12.871 ms          | in 28.614 ms ± 6.949 ms        | in 46.466 ms ± 6.779 ms                   | in 29.009 ms ± 3.134 ms        | in 47.798 ms ± 7.396 ms                   |
| 1.024 kB   | in 17.304 ms ± 3.063 ms      | null                       | in 17.403 ms ± 4.012 ms      | in 25.863 ms ± 6.396 ms           | in 17.792 ms ± 3.643 ms        | in 28.223 ms ± 3.075 ms                   | in 18.381 ms ± 2.783 ms        | in 29.612 ms ± 4.617 ms                   |
| 2.048 kB   | in 22.87 ms ± 5.891 ms       | null                       | in 16.843 ms ± 4.028 ms      | in 34.002 ms ± 6.546 ms           | in 21.91 ms ± 4.232 ms         | in 32.209 ms ± 5.381 ms                   | in 21.76 ms ± 3.26 ms          | in 34.167 ms ± 5.978 ms                   |
| 4.096 kB   | in 24.21 ms ± 2.915 ms       | null                       | in 23.184 ms ± 5.584 ms      | in 41.103 ms ± 5.185 ms           | in 28.046 ms ± 4.162 ms        | in 43.938 ms ± 5.087 ms                   | in 29.164 ms ± 3.233 ms        | in 47.716 ms ± 3.261 ms                   |
| 8.192 kB   | in 38.075 ms ± 6.153 ms      | null                       | in 39.247 ms ± 7.13 ms       | in 57.586 ms ± 2.751 ms           | in 47.613 ms ± 6.414 ms        | in 69.049 ms ± 4.159 ms                   | in 48.339 ms ± 3.38 ms         | in 68.665 ms ± 3.465 ms                   |
| 16.384 kB  | in 57.733 ms ± 4.656 ms      | null                       | in 62.237 ms ± 5.257 ms      | in 112.504 ms ± 3.282 ms          | in 77.924 ms ± 6.425 ms        | in 128.891 ms ± 6.273 ms                  | in 79.183 ms ± 6.307 ms        | in 126.586 ms ± 3.19 ms                   |
| 32.768 kB  | in 92.397 ms ± 4.38 ms       | null                       | in 92.282 ms ± 6.061 ms      | in 191.54 ms ± 9.393 ms           | in 126.66 ms ± 5.315 ms        | in 216.567 ms ± 5.499 ms                  | in 124.705 ms ± 2.328 ms       | in 212.227 ms ± 8.026 ms                  |
| 65.536 kB  | in 175.154 ms ± 3.552 ms     | null                       | in 173.07 ms ± 5.05 ms       | in 351.54 ms ± 19.459 ms          | in 244.786 ms ± 9.103 ms       | in 421.812 ms ± 15.096 ms                 | in 240.165 ms ± 2.607 ms       | in 406.718 ms ± 11.371 ms                 |
| 131.072 kB | in 354.374 ms ± 36.084 ms    | null                       | in 334.968 ms ± 3.282 ms     | in 1,229.626 ms ± 403.301 ms      | in 459.655 ms ± 7.754 ms       | in 1,329.895 ms ± 327.223 ms              | in 464.957 ms ± 6.929 ms       | in 1,448.638 ms ± 303.622 ms              |
| 262.144 kB | in 1,267.741 ms ± 287.749 ms | null                       | in 1,197.067 ms ± 222.294 ms | in 2,438.762 ms ± 617.593 ms      | in 1,662.051 ms ± 253.695 ms   | in 2,650.097 ms ± 550.731 ms              | in 1,665.567 ms ± 212.397 ms   | in 2,574.109 ms ± 369.907 ms              |
| 524.288 kB | in 1,930.775 ms ± 378.425 ms | null                       | in 2,030.34 ms ± 325.556 ms  | in 3,959.315 ms ± 573.141 ms      | in 2,661.78 ms ± 406.668 ms    | in 4,697.064 ms ± 670.256 ms              | in 2,736.744 ms ± 422.099 ms   | in 4,793.741 ms ± 705.207 ms              |
| 1.049 MB   | in 3,600.231 ms ± 274.046 ms | null                       | in 3,653.845 ms ± 441.892 ms | in 7,259.696 ms ± 529.657 ms      | in 4,956.022 ms ± 449.098 ms   | in 8,621.1 ms ± 751.948 ms                | in 5,023.967 ms ± 434.969 ms   | in 8,929.321 ms ± 595.929 ms              |