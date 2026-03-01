1. `&= &{}`

    $$
    \begin{alignat*}{2}
    {} - AC(D,B) + A(C,B)D - C(D,A)B + (C,A)DB  &= &{} - \cancel{ACDB} - \cancel{ACBD} \\
                                                &  &{} + \cancel{ACBD} + ABCD          \\
                                                &  &{} - CDAB          - \cancel{CADB} \\
                                                &  &{} + \cancel{CADB} + \cancel{ACDB} \\\\\\
                                                &= &{} ABCD - CDAB
    \end{alignat*}
    $$

1. ``&= &{-}&\cancel{ACDB}`` aligns in Jekyll

    $$
    \begin{alignat*}{3}
    {} - AC(D,B) + A(C,B)D - C(D,A)B + (C,A)DB  &= &{-}&\cancel{ACDB} - \cancel{ACBD} \\
                                                &  &{+}&\cancel{ACBD} + ABCD          \\
                                                &  &{-}&CDAB          - \cancel{CADB} \\
                                                &  &{+}&\cancel{CADB} + \cancel{ACDB} \\\\\\
                                                &= &   &ABCD - CDAB
    \end{alignat*}
    $$

1. Same as above but narrower width source code

    $$
    \begin{alignat*}{3}
    {} - AC(D,B) + A(C,B)D - C(D,A)B + (C,A)DB  
    &= &{-}&\cancel{ACDB} - \cancel{ACBD} \\
    &  &{+}&\cancel{ACBD} + ABCD          \\
    &  &{-}&CDAB          - \cancel{CADB} \\
    &  &{+}&\cancel{CADB} + \cancel{ACDB} \\\\\\
    &= &   &ABCD - CDAB
    \end{alignat*}
    $$

1. `&= &{-\cancel{ACDB}}&`

    $$
    \begin{alignat*}{3}
    {} - AC(D,B) + A(C,B)D - C(D,A)B + (C,A)DB  &= &{-\cancel{ACDB}}& - \cancel{ACBD} \\
                                                 &  &{+\cancel{ACBD}}& + ABCD          \\
                                                 &  &{-CDAB}&          - \cancel{CADB} \\
                                                 &  &{+\cancel{CADB}}& + \cancel{ACDB} \\\\\\
                                                 &= &{ABCD}&           - CDAB
    \end{alignat*}
    $$

1. `&= &{-\cancel{ACDB}}`

    $$
    \begin{alignat*}{2}
    {} - AC(D,B) + A(C,B)D - C(D,A)B + (C,A)DB  &= &{-\cancel{ACDB}} - \cancel{ACBD} \\
                                                 &  &{+\cancel{ACBD}} + ABCD          \\
                                                 &  &{-CDAB}          - \cancel{CADB} \\
                                                 &  &{+\cancel{CADB}} + \cancel{ACDB} \\\\\\
                                                 &= &{ABCD}           - CDAB
    \end{alignat*}
    $$

1. `&\mathrel{\phantom{=}}` aligns in jekyll

    $$
    \begin{equation*}
    \begin{split}
    {} - AC(D,B) + A(C,B)D - C(D,A)B + (C,A)DB &=                     {} - \cancel{ACDB} - \cancel{ACBD} \\
                                               &\mathrel{\phantom{=}} {} + \cancel{ACBD} +         ABCD  \\
                                               &\mathrel{\phantom{=}} {} -         CDAB  - \cancel{CADB} \\
                                               &\mathrel{\phantom{=}} {} + \cancel{CADB} + \cancel{ACDB} \\\\\\
                                               &=                     {}           ABCD  -         CDAB
    \end{split}
    \end{equation*}
    $$

