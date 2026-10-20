Sinks that compress with `zstd` accept a `window_log` next to `level`, for example `compression = { algorithm = "zstd", level = 9, window_log = 27 }`. A larger window finds repeats further back in the batch, which shrinks the output of large batches at little CPU cost. Readers need a decompression window limit at least as large (zstd's default allows up to 27).

authors: IraSkyx
