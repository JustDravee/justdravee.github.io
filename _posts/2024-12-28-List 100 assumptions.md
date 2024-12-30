---
title: "List: 100 Assumptions That Could Lead to Bugs"
date: 2024-12-29
categories: [state_machine, perspective, finding_bugs]

---

I've been getting questions about assumptions vs invariants, since the following [tweet](https://x.com/BowTiedDravee/status/1872445723985539427). 

ChatGPT provided, surprisingly, a good list (not exhaustive by any means of course but the coverage is quite wide and can give some nice ideas):

## 1. Input-Related Assumptions
1. Users will not pass zero as an input.
2. Users will not pass maximum integer values.
3. Negative numbers are not possible as inputs.
4. Input arrays will always have unique elements.
5. Input strings will not be excessively large.
6. Addresses provided will not be zero address.
7. Addresses provided will not be the contract's own address.
8. Token amounts will not exceed the balance of the sender.
9. Token amounts will not exceed the allowance provided.
10. Numeric inputs will not cause overflows or underflows.
11. Users will not use uninitialized or invalid token contracts.
12. Users will provide valid enum values.
13. Nonces will always increase as intended.
14. Inputs will match expected types (e.g., ETH vs. ERC-20).
15. Users will not duplicate input data.
16. Inputs will not reference non-existent IDs.
17. Inputs will be within specified ranges.
18. Invalid signatures will not be provided.
19. Hashes will match expected input formats.
20. Users will not send mismatched parameter types.

## 2. Call Order-Related Assumptions
21. Functions will always be called in the expected order.
22. Users will not skip initialization steps.
23. Deposits will always occur before withdrawals.
24. Staking will always precede claiming rewards.
25. Users will follow the required sequence for approvals and transfers.
26. State-dependent calls will occur in valid states only.
27. Users will not bypass intermediate validation steps.
28. Admins will set critical parameters before system activation.
29. Initialization will occur exactly once.
30. Reinitialization functions will not be called maliciously.

## 3. External Call-Related Assumptions
31. External contracts will not revert unexpectedly.
32. Tokens will implement the full ERC-20 or ERC-721 standard.
33. Fallback functions will not be exploited.
34. Oracles will provide timely and accurate data.
35. Token transfers will not trigger reentrancy.
36. External data feeds will not be manipulated.
37. Delegated calls will not execute malicious logic.
38. Proxy contracts will point to valid implementations.
39. External dependencies will not be updated unexpectedly.
40. Malicious tokens will not cause denial of service.

## 4. Permission and Role-Related Assumptions
41. Only authorized users will call sensitive functions.
42. Admin roles will not be misassigned.
43. No unauthorized user will gain access to restricted functionality.
44. Privileged roles will not be abused.
45. Ownership transfers will occur securely.
46. Contract migration will preserve permissions correctly.
47. Critical configuration functions will only be accessible to the owner.
48. Time-locked roles will wait for the correct duration.
49. Multisig wallets will function as expected.
50. No privileged roles will perform unexpected actions.

## 5. Economic/Game-Theoretic Assumptions
51. Users will not manipulate rewards for personal gain.
52. Users will not collude to break system fairness.
53. Flash loans will not exploit economic logic.
54. Users will not manipulate auction prices unfairly.
55. Liquidity providers will not abuse fee structures.
56. Validators will not act maliciously to gain rewards.
57. Users will not game staking mechanisms.
58. Governance participants will act in good faith.
59. Incentives will align with intended behaviors.
60. Arbitrage opportunities will not cause systemic loss.

## 6. Time and Sequence-Related Assumptions
61. Block timestamps will not be manipulated.
62. Functions will be called within expected time windows.
63. Timelocks will not be bypassed or miscalculated.
64. Rewards will be claimed in the correct time frame.
65. Events will occur in their expected order.
66. Blocks will be mined at expected intervals.
67. Expiry dates will be enforced correctly.
68. Users will not exploit outdated state between calls.
69. Epoch changes will trigger appropriate state updates.
70. State-dependent functions will execute atomically.

## 7. Math and Precision-Related Assumptions
71. Division operations will not cause rounding errors.
72. Decimal precision will match token standards.
73. Arithmetic operations will not cause overflow.
74. Subtractions will not result in negative balances.
75. Reward calculations will distribute funds accurately.
76. Fees will not reduce balances below zero.
77. Multiplication will not cause unintended scaling.
78. Token amounts will remain within expected precision.
79. Iterative calculations will not lose precision over time.
80. Conversion rates will be consistently applied.

## 8. State and Storage-Related Assumptions
81. State variables will always initialize correctly.
82. Storage reads will reflect the latest state.
83. State transitions will occur atomically.
84. No state updates will be partially applied.
85. Iterative processes will complete in one call.
86. Reserved storage slots will not be overwritten.
87. Contracts will not reference stale or uninitialized variables.
88. Mapping keys will not produce collisions.
89. System state will reflect accurate user balances.
90. Migration processes will transfer state correctly.

## 9. System and Deployment Assumptions
91. Contract addresses will not collide.
92. Proxy deployments will use valid initialization.
93. Libraries will not introduce unexpected behavior.
94. Immutable variables will not be overwritten.
95. Contract deployment order will follow dependencies.
96. Upgrades will preserve existing state and logic.
97. Deployed bytecode will match verified source code.
98. Deployment gas costs will not exceed block limits.
99. Multi-contract systems will synchronize correctly.
100. Contracts will not rely on deprecated or unsupported opcodes.
