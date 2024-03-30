# wcr - Rust implementation of `wc`
A version of the `wc` written in Rust. Used the guide provided in Command-Line Rust written by Ken Youens-Clark

## Examples
```bash
$ cargo run -- --help
```
Running the above command will produce the following result:
```text
Rust version of `wc`

Usage: wcr [OPTIONS] [FILE]...

Arguments:
  [FILE]...  Input file(s) [default: -]

Options:
  -l, --lines    Show line count
  -w, --words    Show word count
  -c, --bytes    Show byte count
  -m, --chars    Show character count
  -h, --help     Print help
  -V, --version  Print version
```
You can then run the tests to see various use cases
```bash
$ cargo test
```
You should see the following result of everything works:
```text
Finished test [unoptimized + debuginfo] target(s) in 0.15s
Running unittests src/main.rs (target/debug/deps/wcr-71e597221340354e)

running 2 tests
test tests::test_format_field ... ok
test tests::test_count ... ok

test result: ok. 2 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s

     Running tests/cli.rs (target/debug/deps/cli-206cf5155e4fd8a9)

running 26 tests
test dies_chars_and_bytes ... ok
test atlamal ... ok
test atlamal_stdin ... ok
test fox_lines ... ok
test empty ... ok
test atlamal_bytes_lines ... ok
test fox_chars ... ok
test atlamal_words_lines ... ok
test fox ... ok
test atlamal_lines ... ok
test atlamal_bytes ... ok
test fox_bytes_lines ... ok
test fox_words ... ok
test fox_bytes ... ok
test atlamal_words_bytes ... ok
test atlamal_words ... ok
test fox_words_bytes ... ok
test fox_words_lines ... ok
test test_all ... ok
test test_all_bytes_lines ... ok
test test_all_bytes ... ok
test skips_bad_file ... ok
test test_all_lines ... ok
test test_all_words ... ok
test test_all_words_bytes ... ok
test test_all_words_lines ... ok

test result: ok. 26 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.29s
```