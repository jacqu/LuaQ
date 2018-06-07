# LuaQ

Special thanks to Patrick Gundlach for his Lua QR code generation code.
(http://speedata.github.com/luaqrcode/)

Features :
- Symbolic responses are evaluated with CAS math engine: robust to equation forms variations
- A tolerance on numerical responses accuracy can be defined
- The quiz result is fed back with a QR code
- Questions and responses may use pretty print display/input math visualizer/editor
- Machine ID is encoded in the QR code
	
Usage: 
- Open LuaQ.tns in the TI-Nspire CX CAS Teacher Software
	- [Insert]->[Script Editor]->[Edit the script]
	- define the quiz in the first table called "QCM_QUESTIONS" in the script
	- if you want textual feedback of the results, define QCM_TEXT_RESULT = 1
	- if you want to associate an alias to the machine ID, define the table QCM_ALIASES
	- result of the test is in the format name, firstname, grade, response pattern, machine ID
	- where :
		- name: response to the first question
		- firstname: response to the second question
		- grade: sum of the points of the good responses
		- response pattern: binary number coding good/false responses, LSB = first question
		- machine ID: unique machine ID, alias if defined or "undefined" on an emulator
	- upload LuaQ.tns to your calculator
- On your calculator, select LuaQ.tns in the file explorer and press [ENTER] 
