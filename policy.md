# Policy of Merge Pull Request

Each type of modification require different policy, the policy is based on
following rules:

## Changes require linker change.
- Require an open source PoC implmenation for `binutils` or `LLD`
  - Available on either mailing list, phabricator or github repo is acceptable.
- Require at least one binutils developer **_AND_** one LLD developer to
  approve.

## Changes require compiler change.
- Require an open source PoC implmenation for `GCC` or `LLVM`
  - Available on either mailing list, phabricator or github repo is acceptable.
- Require at least one GCC developer **_AND_** one LLLVM developer to approve.

## Clarification on current implmenation behavior.
- Require approve from a developer of corresponding component.

## General document improvement and clarification.
- One of the following approve:
 - Andrew Waterman (@aswaterman)
 - Jessica Clarke (@jrtc27)
 - Jim Wilson (@jim-wilson)
 - Kito Cheng (@kito-cheng)
 - Palmer Dabbelt (@palmer-dabbelt)

## Do **_NOT_** make incompatible change.
- Incompatible are generally unexpectable.
- In case, it's a ABI bug fix or a very conner case, it require at
  least two of following approve:
 - Andrew Waterman (@aswaterman)
 - Jessica Clarke (@jrtc27)
 - Jim Wilson (@jim-wilson)
 - Kito Cheng (@kito-cheng)
 - Palmer Dabbelt (@palmer-dabbelt)

# When do I need to modify compiler and/or linker?
Change or add new stuffs to the ELF format require linker
change, e.g. new relocation type, new flags for e_flags field.

Change or add new ABI, new calling convention or new code model require compiler
change.

# Where can I find a RISC-V GCC/LLVM/binutils/LLD developers?
Here is an incomplete list for those developers, but not limited to following
list.
- Andrew Waterman (@aswaterman): GCC
- Jim Wilson (@jim-wilson): GCC/binutils
- Kito Cheng (@kito-cheng): GCC
- Palmer Dabbelt (@palmer-dabbelt): binutils
- Nelson Chu (@Nelson1225): binutils
- Alex Bradbury (@asb): LLVM
- Evandro Menezes (@ebahapo): LLVM
- PkmX (@PkmX): LLD
- Jessica Clarke (@jrtc27): LLD
- Fangrui Song (@Maskray): LLVM/LLD
