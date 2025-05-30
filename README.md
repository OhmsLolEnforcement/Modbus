# Modbus
The purpose of this project is to create a tool for reading and logging Modbus data as a client, then eventually serving time-series data as a server.
Tools exist that already do this, however they lack the speed, flexibility and integration with my other projects.
I am separately working on a home-grown power plant controller (PPC) for solar power plants, built in Function Blocks and Structured Text. This PPC operates on both OpenPLC and SEL RTAC.
Testing this PPC is quite challenging since it requires closed-loop controls. I have also developed a solar farm simulator with inverter P/Q curves, apparent power limits and temperature derating, but simulating realistic performance requires feeding this simulator with real-world irradiance data.

Roadmap:
0.1 : Learn PyModbus to the extent that we can reliably read binary inputs, signed integers, unsigned integers, 32-bit floats and 32-bit unsigned integers as bitmapped alarms.
0.2 : Learn pyModbus to the extent that we can write the same datatypes (plus coils).
0.3 : Save values of all parameters to a time-series database.
0.4 : Create an auto-configurator to parse a list of parameters and metadata from an excel spreadsheet and synthesize a matching Modbus Server.
0.5 : Create a Modbus client application that is able to serve or write 1-second data from a database or excel spreadsheet.
