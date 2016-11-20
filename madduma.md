# LLVM -O2 optimizations

The following is a sequence of optimization applied on the LLVM IR by the LLVM optimizer at level -O2. The repeated optimizations belong to different passes. 

  - Module Verifier
  - Simplify the CFG
  - SROA
  - Lower 'expect' Intrinsics
  - Force set function attributes
  - Infer set function attributes
  - Interprocedural Sparse Conditional Constant Propagation
  - Global Variable Optimizer
  - Promote Memory to Register
  - Dead Argument Elimination 
  - Simplify the CFG
  - PGOIndirectCallPromotion
  - Remove unused exception handling info 
  - Function Integration/Inlining
  - Deduce function attributes
  - Remove unused exception handling info
  - Function Integration/Inlining
  - After Deduce function attributes
  - Remove unused exception handling info
  - Function Integration/Inlining
  - Deduce function attributes 
  - SROA
  - Early CSE
  - Speculatively execute instructions if target has divergent branches
  - Jump Threading
  - Value Propagation
  - Simplify the CFG
  - Reassociate expressions 
  - Canonicalize natural loops
  - Loop-Closed SSA Form Pass
  - Rotate Loops
  - Loop Invariant Code Motion
  - Unswitch loops
  - Combine redundant instructions
  - Canonicalize natural loops
  - Loop-Closed SSA Form Pass
  - Induction Variable Simplification
  - Recognize loop idioms
  - Delete dead loops
  - Unroll loops
  - MergedLoadStoreMotion
  - Global Value Numbering 
  - MemCpy Optimization
  - Sparse Conditional Constant Propagation 
  - Demanded bits analysis
  - Bit-Tracking Dead Code Elimination
  - Combine redundant instructions
  - Jump Threading
  - Value Propagation
  - Dead Store Elimination
  - Canonicalize natural loops
  - Loop-Closed SSA Form Pass
  - Loop Invariant Code Motion
  - Simplify the CFG 
  - Combine redundant instructions
  - Remove unused exception handling info 
  - Function Integration/Inlining
  - Deduce function attributes
  - Remove unused exception handling info
  - Function Integration/Inlining
  - After Deduce function attributes
  - Remove unused exception handling info
  - Function Integration/Inlining
  - Deduce function attributes 
  - No-Op Barrier Pass 
  - Eliminate Available Externally Globals
  - Deduce function attributes in RPO
  - Float to int
  - Canonicalize natural loops
  - Loop-Closed SSA Form Pass
  - Rotate Loops
  - Loop Distribition
  - Canonicalize natural loops
  - Loop-Closed SSA Form Pass
  - Demanded bits analysis
  - Loop Vectorization
  - Canonicalize natural loops
  - Loop Load Elimination
  - Combine redundant instructions
  - Demanded bits analysis
  - SLP Vectorizer
  - Simplify the CFG
  - Combine redundant instructions
  - Canonicalize natural loops
  - Loop-Closed SSA Form Pass
  - Unroll loops
  - Combine redundant instructions
  - Canonicalize natural loops
  - Loop-Closed SSA Form Pass
  - Loop Invariant Code Motion
  - Remove redundant instructions
  - Alignment from assumptions
  - Strip Unused Function Prototypes
  - Dead Global Elimination
  - Merge Duplicate Global Constants
  - Module Verifier

****

Original program `power.calc`

    (seq (set a0 m0)
         (seq (set a1 m1)
              (while (!= m1 1)
                     (seq (set (* m0 a0) m0)
                          (seq (set (- m1 1) m1) m0)))))





















