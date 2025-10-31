---
layout: post
title: Linear Algebra - some notes
---


# Upcoming Linear Algebra Midterm Test

I haven't prepared well for it. I wish it will be a good result.

## Some rank inequalities
- $r(\mathbf{AB}) \leq min \left\\{ r(\mathbf{A}), r(\mathbf{B}) \right\\} $
- $r(\mathbf{A}) = r(\mathbf{A^{T}}) = r(\mathbf{AA^{T}})$
- $r(\mathbf{A + B}) \leq r(\mathbf{A}) + r(\mathbf{B}) \leq n + r(\mathbf{AB})$ (sylvester rank inequality)
- $r(\mathbf{ABC}) +r(\mathbf{B}) \geq r(\mathbf{AB}) + r(\mathbf{BC}) $ (Frobenius rank inequality)

## Some euqalities
- $(A-BDC)^{-1} = A^{-1} - A^{-1}B(D^{-1}+CA^{-1}B)^{-1} CA^{-1} $ (Woodbury equality)
- $((A-B^{-1})-A^{-1})^{-1} = ABA-A $ (Hua's equality)
