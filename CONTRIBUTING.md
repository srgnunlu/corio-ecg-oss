# Contributing

Use a `feature/...` branch and explain the problem, proposed change, and validation
in a pull request. Preserve upstream attribution and license notices.

For bug reports, provide a minimal reproduction using synthetic input. Do not
include real patient information, identifiable clinical images, access-controlled
datasets, private file paths, credentials, or raw application logs.

For changes to measurements or evaluation code, explain the expected behavior and
add a focused regression test. Report software behavior separately from clinical
performance; do not infer clinical validation from passing unit tests.

Run the tests relevant to the change and document any unavailable external model
or dataset dependency. Avoid adding generated results or model weights to Git.
