# non-text nodes in links fails

    Code
      (expect_error(markdown("[`foo` bar][x]"), "plain text"))
    Output
      <error/rlang_error>
      Error: Links must contain plain text.
      x Problematic node: `code`
      i Link target: `x`
    Code
      (expect_error(markdown("[`foo{}` bar __baz__][x]"), "plain text"))
    Output
      <error/rlang_error>
      Error: Links must contain plain text.
      x Problematic nodes: `code` and `strong`
      i Link target: `x`

