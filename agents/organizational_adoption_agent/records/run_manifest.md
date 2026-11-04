# Specialist execution manifest

Six separate guest ChatGPT conversations on November 3, 2026. Guest conversation identifiers are provenance markers and may be inaccessible outside the original session. Rebuild each packet with the supplied prompt builder and the corresponding versioned instructions, metadata and unchanged case. SHA-256 digests are for complete packet and preserved response bytes.

| Version | Case | Conversation ID | Packet SHA-256 | Response SHA-256 | Frozen validator |
|---|---|---|---|---|---|
| 0.1 | primary | `6aea8895-4628-83ea-b17e-f09f0e2fe093` | `82ddaad26b9d9203fb7baa6ae1ab1306cebd169b2541f5e26a352c26e1abfe6b` | `fc207f3c41c21f6d7f3a8397a61cd675fda54186c7fa3f1c366460956571b926` | PASS |
| 0.1 | contrast_1 | `6aea88ac-a8d0-83ea-9d9a-684513dc5bef` | `bbfb79d1ae0ccdd6ae42fcda2a47476956e9cd7287ff4a4058fe3242ee2d4860` | `3b3a8c670894aa7d95843a4d5ea0e860e9e782616e0b0f159063366abf5981c7` | PASS |
| 0.1 | contrast_2 | `6aea88ac-4a50-83ea-9738-04d263d69699` | `99b3266a565346d85bd8c874016d49bd00646ae5c70a5e38f55f66bf8fe60aaf` | `708a4761ad4847511ba34046d55fb73c91dcf676b0930d6591b9f8befeca4536` | PASS |
| 0.2 | primary | `6aea8911-f238-83ea-925b-7f8dabfb1065` | `2d8814cd92ce1c457705bc81def8272f0d3796942e78108b8f00c44495acc2ef` | `a35ef8fcbdf092646794c05128b8689d664e63f6fd83bbb055c46c7e230693f1` | PASS |
| 0.2 | contrast_1 | `6aea8911-9280-83ea-8859-7ee8d1afffa8` | `0a9dfc6775b13f58cfb0f1df54295e7b8087148d8997243612cdec58112a351e` | `52eaf06a609f3155900560111307575374ee30421f7b403b483c402225735149` | PASS |
| 0.2 | contrast_2 | `6aea8910-d140-83ea-a443-2f150dd83fc0` | `29fcb8355ddbd320c0df0961dd6651908aee8c05bff98e50ec70136887a460a0` | `d30506da3aaf2e319acfaa9ba74c85d11961f0e6c9413af4f9b1446f2c8403e5` | PASS |

## November 4, 2026 format retest

Three separate guest ChatGPT conversations used the default model. The interface did not expose its build. The tested instructions and metadata are at `ca160daad266f8cc02739b9aad81e5250cbc1d2c`. Raw responses were preserved from the completed rendered JSON without repair.

| Version | Case | Conversation ID | Packet SHA-256 | Response SHA-256 | Instructor validator | Draft 2020-12 |
|---|---|---|---|---|---|---|
| 0.3 | primary | `6aeba59b-aa98-83ea-8a35-f9c5f903a2a7` | `5437de61fb6efbd66ad29390b59a36b961593af42b5df0c36a839389d16c4ddb` | `2408ed159e835c4db2abde151188cbe08988f452f3afae7545ee385fc590b6cd` | PASS | PASS |
| 0.3 | contrast_1 | `6aeba5ae-87dc-83ea-8166-8218d63faeaa` | `3ebe7b27e0f696ec8e037c2f57532481410efa154a8112a436e4d2cbaada813c` | `2c179ff6223e323df3495aec075e2e741eb6c47a631b28f96ad5d1a4d95361d9` | PASS | PASS |
| 0.3 | contrast_2 | `6aeba5af-393c-83ea-879e-df0bd9127fc5` | `38dc212d95109cd4943f3498863c2ea9546ddb9efa51e38d57212a994d6a5de8` | `032618f42938fd432ca622aad80770fba3ea974bea1cccf71c02dc082569cdfb` | PASS | PASS |
