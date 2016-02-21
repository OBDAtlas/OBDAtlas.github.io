---
title: PIDs
layout: page
document_type: pid
mode: 09
permalink: resources/pids/01/c0.html
description: Mode 9 pids
---

PID
(hex)	Data bytes returned	Description	Min value	Max value	Units	Formula[a]
00	4	Mode 9 supported PIDs (01 to 20)				Bit encoded. [A7..D0] = [PID $01..PID $20] See below
01	1	VIN Message Count in PID 02. Only for ISO 9141-2, ISO 14230-4 and SAE J1850.				Usually value will be 5.
02	17-20	Vehicle Identification Number (VIN)				17-char VIN, ASCII-encoded and left-padded with null chars (0x00) if needed to.
03	1	Calibration ID message count for PID 04. Only for ISO 9141-2, ISO 14230-4 and SAE J1850.				It will be a multiple of 4 (4 messages are needed for each ID).
04	16	Calibration ID				Up to 16 ASCII chars. Data bytes not used will be reported as null bytes (0x00).
05	1	Calibration verification numbers (CVN) message count for PID 06. Only for ISO 9141-2, ISO 14230-4 and SAE J1850.				
06	4	Calibration Verification Numbers (CVN)				Raw data left-padded with null characters (0x00). Usually displayed as hex string.
07	1	In-use performance tracking message count for PID 08 and 0B. Only for ISO 9141-2, ISO 14230-4 and SAE J1850.	8	10		8 if sixteen (16) values are required to be reported, 9 if eighteen (18) values are required to be reported, and 10 if twenty (20) values are required to be reported (one message reports two values, each one consisting in two bytes).
08	4	In-use performance tracking for spark ignition vehicles				4 or 5 messages, each one containing 4 bytes (two values). See below
09	1	ECU name message count for PID 0A				
0A	20	ECU name				ASCII-coded. Right-padded with null chars (0x00).
0B	4	In-use performance tracking for compression ignition vehicles				5 messages, each one containing 4 bytes (two values). See below
