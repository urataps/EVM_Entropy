# Entropy Analysis of Smart Contracts EVM opcodes



`entropy.py`calculates number of occurrences of each mnemonic in the contracts from the `contracts/` folder. There are 50 contracts taken from etherescan.io. Before running the script make sure you installed the EVM disassembler, you can do that using `pip install pyevmasm`. At operations that have a dynamic gas cost (a formula calculating it) their minimum was taken.


#Results:
| Mnemonics| Occurences | Gas Cost | Gas Spent | Occ. per Contract
  --- | --- | --- | --- | ---
PUSH1|118464|3|355392|2369.28
PUSH2|48963|3|146889|979.26
SWAP1|48165|3|144495|963.3
DUP1|47523|3|142569|950.46
POP|44334|2|88668|886.68
DUP2|40002|3|120006|800.04
ADD|38373|3|115119|767.46
JUMPDEST|33591|1|33591|671.82
MSTORE|29046|3|87138|580.92
AND|21474|3|64422|429.48
MLOAD|20520|3|61560|410.4
ISZERO|20154|3|60462|403.08
JUMPI|20049|10|200490|400.98
SWAP2|19059|3|57177|381.18
DUP3|18066|3|54198|361.32
JUMP|16089|8|128712|321.78
SUB|12885|3|38655|257.7
SLOAD|11676|200|2335200|233.52
REVERT|11001|0|0|220.02
DUP4|10815|3|32445|216.3
PUSH20|10080|3|30240|201.6
STOP|8394|0|0|167.88
PUSH4|8229|3|24687|164.58
SWAP3|7530|3|22590|150.6
SHA3|6087|30|182610|121.74
EQ|5373|3|16119|107.46
MUL|5067|5|25335|101.34
SHL|5010|3|15030|100.2
SSTORE|4884|5000|24420000|97.68
LT|4602|3|13806|92.04
DUP5|4428|3|13284|88.56
DIV|3981|5|19905|79.62
PUSH3|3897|3|11691|77.94
CALLDATALOAD|3672|3|11016|73.44
EXP|3633|10|36330|72.66
INVALID|3351|0|0|67.02
RETURNDATASIZE|3102|2|6204|62.04
PUSH32|2805|3|8415|56.1
DUP6|2793|3|8379|55.86
GT|2727|3|8181|54.54
CALLVALUE|2646|2|5292|52.92
CALLER|2478|2|4956|49.56
NOT|2406|3|7218|48.12
SWAP4|2148|3|6444|42.96
OR|2064|3|6192|41.28
DUP7|2001|3|6003|40.02
RETURN|1857|0|0|37.14
DUP8|1758|3|5274|35.16
CALLDATASIZE|1548|2|3096|30.96
EXTCODESIZE|1170|700|819000|23.4
CODECOPY|1167|2|2334|23.34
GAS|1167|2|2334|23.34
RETURNDATACOPY|1149|3|3447|22.98
DUP9|1020|3|3060|20.4
CALL|909|Complex| N\A |18.18
SWAP5|903|3|2709|18.06
DUP10|783|3|2349|15.66
ADDRESS|651|2|1302|13.02
SWAP6|567|3|1701|11.34
LOG3|525|1500|787500|10.5
PUSH5|447|3|1341|8.94
DUP11|435|3|1305|8.7
TIMESTAMP|411|2|822|8.22
STATICCALL|390|40|15600|7.8
SHR|327|3|981|6.54
PUSH8|303|3|909|6.06
PUSH29|300|3|900|6.0
DUP12|285|3|855|5.7
CALLDATACOPY|285|2|570|5.7
LOG1|276|750|207000|5.52
LOG2|267|1125|300375|5.34
PUSH16|252|3|756|5.04
PUSH6|210|3|630|4.2
SLT|192|3|576|3.84
SWAP7|186|3|558|3.72
SWAP8|174|3|522|3.48
XOR|165|3|495|3.3
PUSH7|162|3|486|3.24
PUSH21|144|3|432|2.88
MOD|144|5|720|2.88
NUMBER|141|2|282|2.82
PUSH19|138|3|414|2.76
PUSH15|138|3|414|2.76
ORIGIN|135|2|270|2.7
DUP13|135|3|405|2.7
GASPRICE|129|2|258|2.58
DUP14|126|3|378|2.52
GASLIMIT|96|2|192|1.92
CODESIZE|96|2|192|1.92
PUSH22|78|3|234|1.56
PUSH28|78|3|234|1.56
DUP15|78|3|234|1.56
SWAP9|75|3|225|1.5
BALANCE|75|400|30000|1.5
SWAP13|72|3|216|1.44
SDIV|66|5|330|1.32
PUSH27|63|3|189|1.26
MSTORE8|63|3|189|1.26
SWAP11|63|3|189|1.26
SWAP10|63|3|189|1.26
PUSH12|60|3|180|1.2
GETPC|60|2|120|1.2
PUSH10|60|3|180|1.2
PUSH9|51|3|153|1.02
DELEGATECALL|51|Complex| N\A |1.02
PUSH13|48|3|144|0.96
PUSH17|48|3|144|0.96
PUSH24|48|3|144|0.96
BLOCKHASH|42|20|840|0.84
DUP16|42|3|126|0.84
LOG4|42|1875|78750|0.84
PUSH25|42|3|126|0.84
DIFFICULTY|39|2|78|0.78
PUSH18|36|3|108|0.72
CREATE2|36|32000|1152000|0.72
CREATE|33|32000|1056000|0.66
SAR|33|3|99|0.66
SWAP12|33|3|99|0.66
SWAP14|30|3|90|0.6
PUSH14|30|3|90|0.6
MSIZE|27|2|54|0.54
PUSH11|27|3|81|0.54
PUSH26|21|3|63|0.42
SIGNEXTEND|21|5|105|0.42
SGT|21|3|63|0.42
PUSH31|21|3|63|0.42
ADDMOD|18|8|144|0.36
BYTE|18|3|54|0.36
LOG0|18|375|6750|0.36
SMOD|18|5|90|0.36
SELFDESTRUCT|18|25000|450000|0.36
COINBASE|18|2|36|0.36
PUSH23|18|3|54|0.36
MULMOD|15|8|120|0.3
EXTCODEHASH|15|700|10500|0.3
SWAP16|15|3|45|0.3
PUSH30|12|3|36|0.24
EXTCODECOPY|9|700|6300|0.18
CALLCODE|9|Complex| N\A |0.18
SWAP15|3|3|9|0.06
