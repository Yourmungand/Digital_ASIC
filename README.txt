The archive contains source files and scripts needed to build ASIC design of DC removal and Envelope Detector modules, which is originally was built in MATLAB Simulink. The archive contains the folowing folders and files:

Digital_ASIC:
	Logs:
		encounter.log		# log file from Cadence Encounter
		qrc.log			# log file for QRC
		rc.log			# log file for RC extraction
	Outputs:
		DesignConstraints.sdc		# Constraints for design
		ToVerilog.def		# topology file from Encounter
		DC_Env.sdf		# sdf file from encounter	
		ToVerilog.v	# generated logic netlist
		ToVerilog_phys.v	# generated physical netlist
		FI_Full_synth.v	# generated netlist by RTL Compiler
	Reports:
		Encounter:
			# Reports for Hold and Setup Violations from Encounter:
			postCTS:
				ToVerilog_postCTS.summary
				ToVerilog_postCTS_hold.summary
			postRoute:
				ToVerilog_postRoute.summary
				ToVerilog_postRoute_hold.summary
			preCTS:
				ToVerilog_preCTS.summary
				ToVerilog_preCTS_hold.summary			
			signoff:
				ToVerilog_signOff.summary
				ToVerilog_signOff_hold.summary
		RTL_Compiler:
			# Timing and area reports from RTL Compiler
			FI_Full_area_report
			FI_Full_timing_report
	Scripts:
		ToVerilog_PaR.tcl		# PaR script
		Module_pins.tcl		# IO assignment
		MyModule_syn.tcl		# script for RTL compiler
		MMMC.tcl		# technology script
		XFAB_fast.tcl		# tcl script for fast corner
		XFAB_slow.tcl		# tcl script for fast slow
		XFAB_typ.tcl		# tcl script for fast tupical
	Source:
		GilbertTransformer.v	# Gilbert Transform module
		DC_and_EnvDet_TB.v		# original testbench
		ToVerilog.v			# Top module
		DataIn.txt			# input signal
		DC_Out.txt		# output signal (DC removal filter)
		Env_Out.txt		# output signal (EnvelopeDetector)
		Subsystem.v			# submodule
		EnvelopeDetection       #Envelope Detector module
                DC_filter               #DC removal module
                FI_Full1                #Submodule