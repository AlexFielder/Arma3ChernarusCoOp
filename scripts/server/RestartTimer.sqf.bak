private ['_restartTime', '_msgTimes', '_msgFormat'];
_restartTime = 361;
_msgTimes = [1,5,10,15,30,45,60,90,120];
_msgFormaty = "<t size='0.60' color='#f2cb0b' align='right'>RESTART IN %1 MINS</t>";
_msgFormatg = "<t size='0.60' color='#00ff00' align='right'>RESTART IN %1 MINS</t>";
_msgFormatr = "<t size='0.60' color='#ff0000' align='right'>RESTART IN %1 MINS</t>";
_msgFormatb = "<t size='0.60' color='#0000ff' align='right'>RESTART IN %1 MINS</t>";

while {true} do {
	uiSleep 30;
	if ((_restartTime - floor(serverTime / 60)) in _msgTimes) then {

		_msgTimes = _msgTimes - [(_restartTime - floor(serverTime / 60))];
		_restartIn = (_restartTime - floor(serverTime / 60));

		for "_i" from 1 to 3 do {
		[
			format[_msgFormaty, _restartIn],
			[safezoneX + safezoneW - 0.8,0.50],
			[safezoneY + safezoneH - 0.8,0.7],
			3,
			0.2
		] spawn BIS_fnc_dynamicText;
		uisleep 2;
		[
			format[_msgFormatg, _restartIn],
			[safezoneX + safezoneW - 0.8,0.50],
			[safezoneY + safezoneH - 0.8,0.7],
			3,
			0.2
		] spawn BIS_fnc_dynamicText;
		uisleep 2;
		[
			format[_msgFormatr, _restartIn],
			[safezoneX + safezoneW - 0.8,0.50],
			[safezoneY + safezoneH - 0.8,0.7],
			3,
			0.2
		] spawn BIS_fnc_dynamicText;
		uisleep 2;
		[
			format[_msgFormatb, _restartTime - floor(serverTime / 60)],
			[safezoneX + safezoneW - 0.8,0.50],
			[safezoneY + safezoneH - 0.8,0.7],
			3,
			0.2
		] spawn BIS_fnc_dynamicText;
	};
	};
};