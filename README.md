screenshots of opening openlane

![image_alt](https://github.com/mishika20/openlane-working-dir/blob/6773a00cc4b516c72cae71098e071bc402531ed4/Screenshot%20from%202025-01-28%2012-11-47.png)
![image_alt](https://github.com/mishika20/openlane-working-dir/blob/6773a00cc4b516c72cae71098e071bc402531ed4/Screenshot%20from%202025-01-28%2012-13-53.png)

openlane components

![image_alt](https://github.com/mishika20/openlane-working-dir/blob/6773a00cc4b516c72cae71098e071bc402531ed4/Screenshot%20from%202025-01-28%2012-17-13.png)

different designs present...whole list

![image_alt](https://github.com/mishika20/openlane-working-dir/blob/6773a00cc4b516c72cae71098e071bc402531ed4/Screenshot%20from%202025-01-28%2012-17-27.png)

the desigm picorv32a on which we will work... 

components of the design picorv32a
![image_alt](https://github.com/mishika20/openlane-working-dir/blob/6773a00cc4b516c72cae71098e071bc402531ed4/Screenshot%20from%202025-01-28%2012-17-31.png)
![image_alt](https://github.com/mishika20/openlane-working-dir/blob/6773a00cc4b516c72cae71098e071bc402531ed4/Screenshot%20from%202025-01-28%2012-17-35.png)

now the design is prepped and ready, we run synthesis using following command ..... run_synthesis
![image_alt](https://github.com/mishika20/openlane-working-dir/blob/199d24b84a6c518b00a6413630dc50fc5bcd1897/Screenshot%20from%202025-01-28%2013-27-50.png)

calculate the flop ratio
screenshot of synthesis statistics with required values highlighted
![image_alt](https://github.com/mishika20/openlane-working-dir/blob/8ce9be09d77eefaa9f1598291520edc804d08b07/Screenshot%20from%202025-01-29%2016-11-06.png)
![image_alt](https://github.com/mishika20/openlane-working-dir/blob/8ce9be09d77eefaa9f1598291520edc804d08b07/Screenshot%20from%202025-01-29%2016-11-43.png)
calculation of flop ratio and dff from report

flop ratio = 1613 / 14876 = 0.108429685 

percentage of DFF = 0.108429685* 100 = 10.8429685

now we can run floorplan
run_floorplan
screenshots of floorplan run
![image_alt](https://github.com/mishika20/openlane-working-dir/blob/8ce9be09d77eefaa9f1598291520edc804d08b07/Screenshot%20from%202025-01-29%2016-15-28.png)
![image_alt](https://github.com/mishika20/openlane-working-dir/blob/8ce9be09d77eefaa9f1598291520edc804d08b07/Screenshot%20from%202025-01-29%2016-14-52.png)
![image_alt](https://github.com/mishika20/openlane-working-dir/blob/8ce9be09d77eefaa9f1598291520edc804d08b07/Screenshot%20from%202025-01-29%2016-24-28.png)
![image_alt](https://github.com/mishika20/openlane-working-dir/blob/8ce9be09d77eefaa9f1598291520edc804d08b07/Screenshot%20from%202025-01-29%2016-35-19.png)
![image_alt](https://github.com/mishika20/openlane-working-dir/blob/8ce9be09d77eefaa9f1598291520edc804d08b07/Screenshot%20from%202025-01-29%2016-41-58.png)
![image_alt](https://github.com/mishika20/openlane-working-dir/blob/8ce9be09d77eefaa9f1598291520edc804d08b07/Screenshot%20from%202025-01-29%2016-45-45.png)
calculate the die area in microns from the values in floorplan def
screenshot of contents of floorplan def
![image_alt](https://github.com/mishika20/openlane-working-dir/blob/8ce9be09d77eefaa9f1598291520edc804d08b07/Screenshot%20from%202025-01-29%2016-49-13.png)
according to foorplan def

1000 unit distance = 1 Micron

die width in unit distance = 660685

die height in unit distance = 671405

distance in microns = value in unit distance/ 1000

die width = 660685/1000 = 660.685 Micron

die height = 671405/1000 = 671.405 Micron

area of die in micron = 660.685 * 671.405 = 443587.2124 Square Micron

Commands to load floorplan def in magic 
magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.floorplan.def &

screenshots of floorplan def in magic
![image_alt](https://github.com/mishika20/openlane-working-dir/blob/8ce9be09d77eefaa9f1598291520edc804d08b07/Screenshot%20from%202025-01-29%2016-58-09.png)

press s then v to keep this in centre
![image_alt](https://github.com/mishika20/openlane-working-dir/blob/8ce9be09d77eefaa9f1598291520edc804d08b07/Screenshot%20from%202025-01-29%2016-59-18.png)
![image_alt](https://github.com/mishika20/openlane-working-dir/blob/8ce9be09d77eefaa9f1598291520edc804d08b07/Screenshot%20from%202025-01-29%2017-02-18.png)
![image_alt](https://github.com/mishika20/openlane-working-dir/blob/8ce9be09d77eefaa9f1598291520edc804d08b07/Screenshot%20from%202025-01-29%2017-05-19.png)
![image_alt](https://github.com/mishika20/openlane-working-dir/blob/8ce9be09d77eefaa9f1598291520edc804d08b07/Screenshot%20from%202025-01-29%2017-06-23.png)
![image_alt](https://github.com/mishika20/openlane-working-dir/blob/8ce9be09d77eefaa9f1598291520edc804d08b07/Screenshot%20from%202025-01-29%2017-07-51.png)
![image_alt](https://github.com/mishika20/openlane-working-dir/blob/8ce9be09d77eefaa9f1598291520edc804d08b07/Screenshot%20from%202025-01-29%2017-11-02.png)
![image_alt](https://github.com/mishika20/openlane-working-dir/blob/8ce9be09d77eefaa9f1598291520edc804d08b07/Screenshot%20from%202025-01-29%2017-12-23.png)
![image_alt](https://github.com/mishika20/openlane-working-dir/blob/8ce9be09d77eefaa9f1598291520edc804d08b07/Screenshot%20from%202025-01-29%2017-14-38.png)

command to run placement run_placement
screenshot of placement run
![image_alt](https://github.com/mishika20/openlane-working-dir/blob/8ce9be09d77eefaa9f1598291520edc804d08b07/Screenshot%20from%202025-01-29%2020-34-31.png)
command to load placement def in magic 
magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.placement.def &

Screenshot of floorplan def in magic
![image_alt](https://github.com/mishika20/openlane-working-dir/blob/8ce9be09d77eefaa9f1598291520edc804d08b07/Screenshot%20from%202025-01-29%2020-32-13.png)
![image_alt](https://github.com/mishika20/openlane-working-dir/blob/8ce9be09d77eefaa9f1598291520edc804d08b07/Screenshot%20from%202025-01-29%2020-32-26%20-%201.png)
![image_alt](https://github.com/mishika20/openlane-working-dir/blob/8ce9be09d77eefaa9f1598291520edc804d08b07/Screenshot%20from%202025-01-29%2020-32-26%20-%202.png)

Clone custom inverter standard cell design from github repository
command is
git clone https://github.com/nickson-jose/vsdstdcelldesign

screenshot showing clone and changing directory as well as the copying the file

![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/6227e8149f7aad3a9dcd9fd613c18befb371203e/Screenshot%20from%202025-01-29%2022-13-23.png)
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/6227e8149f7aad3a9dcd9fd613c18befb371203e/Screenshot%20from%202025-01-29%2022-24-12.png)
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/6227e8149f7aad3a9dcd9fd613c18befb371203e/Screenshot%20from%202025-01-29%2022-24-25.png)

command to open custom inverter layout in magic

magic -T sky130.tech sky130_inv.mag &

screenshot of custom inverter layout in magic

![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/6227e8149f7aad3a9dcd9fd613c18befb371203e/Screenshot%20from%202025-01-29%2022-27-37.png)
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/6227e8149f7aad3a9dcd9fd613c18befb371203e/Screenshot%20from%202025-01-29%2022-28-03.png)

NMOS and PMOS identified

![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/911d1eeced064ec146e7fb4f9887a187ed14a13f/Screenshot%20from%202025-01-29%2023-01-55.png)
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/911d1eeced064ec146e7fb4f9887a187ed14a13f/Screenshot%20from%202025-01-29%2023-02-26.png)

Output Y connectivity to PMOS and NMOS drain verified

![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/911d1eeced064ec146e7fb4f9887a187ed14a13f/Screenshot%20from%202025-01-29%2023-05-29.png)

PMOS source connectivity to VDD verified
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/911d1eeced064ec146e7fb4f9887a187ed14a13f/Screenshot%20from%202025-01-29%2023-05-47.png)

NMOS source connectivity to VSS verified
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/911d1eeced064ec146e7fb4f9887a187ed14a13f/Screenshot%20from%202025-01-29%2023-05-59.png)

SPICE EXTRACTION
screenshot of tkcon window

![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/d419b86a029e15e81a8c4ca54d0c867cfe94debb/Screenshot%20from%202025-01-29%2023-28-12.png)
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/d419b86a029e15e81a8c4ca54d0c867cfe94debb/Screenshot%20from%202025-01-29%2023-25-22.png)
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/d419b86a029e15e81a8c4ca54d0c867cfe94debb/Screenshot%20from%202025-01-29%2023-28-53.png)

![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/d419b86a029e15e81a8c4ca54d0c867cfe94debb/Screenshot%20from%202025-01-29%2023-30-35.png)

changes made in the spice file
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/d419b86a029e15e81a8c4ca54d0c867cfe94debb/Screenshot%20from%202025-01-30%2009-44-34.png)

then run ngspice, for that ngspice need to be installed 

![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/d419b86a029e15e81a8c4ca54d0c867cfe94debb/Screenshot%20from%202025-01-30%2000-46-04.png)
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/d419b86a029e15e81a8c4ca54d0c867cfe94debb/Screenshot%20from%202025-01-30%2000-45-57.png)

![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/a3a42f115dadf49aff66708da104e4018b727d44/Screenshot%202025-01-30%20094331.png)

CONDITIONS TO BE VERIFIED BEFORE MOVING FORWARD WITH CUSTOM DESIGNED CELL LAYOUT

![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/b5cf657956babe382f2597d73906074a9b48cccd/Screenshot%20from%202025-01-30%2015-43-37.png)

CONDITION 1 VERIFIED

![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/b5cf657956babe382f2597d73906074a9b48cccd/Screenshot%20from%202025-01-30%2015-47-19.png)
CONDITION 2 VERIFIED 
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/b5cf657956babe382f2597d73906074a9b48cccd/Screenshot%20from%202025-01-30%2016-03-25.png)

![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/b5cf657956babe382f2597d73906074a9b48cccd/Screenshot%20from%202025-01-30%2015-47-07.png)

![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/b5cf657956babe382f2597d73906074a9b48cccd/Screenshot%20from%202025-01-30%2016-01-16.png)

![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/b5cf657956babe382f2597d73906074a9b48cccd/Screenshot%20from%202025-01-30%2016-05-54.png)
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/b5cf657956babe382f2597d73906074a9b48cccd/Screenshot%20from%202025-01-30%2016-07-07.png)
command magic -T sky130A.tech sky130_vsdinv.mag &
SCREENSHOT OF NEWLY SAVED LAYOUT
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/b5cf657956babe382f2597d73906074a9b48cccd/Screenshot%20from%202025-01-30%2016-11-08.png)

![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/b5cf657956babe382f2597d73906074a9b48cccd/Screenshot%20from%202025-01-30%2016-11-30.png)

![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/b5cf657956babe382f2597d73906074a9b48cccd/Screenshot%20from%202025-01-30%2016-15-22.png)

![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/b5cf657956babe382f2597d73906074a9b48cccd/Screenshot%20from%202025-01-30%2016-34-48.png)
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/b5cf657956babe382f2597d73906074a9b48cccd/Screenshot%20from%202025-01-30%2016-34-57.png)
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/b5cf657956babe382f2597d73906074a9b48cccd/Screenshot%20from%202025-01-30%2017-13-35.png)

config.tcl file

![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/b5cf657956babe382f2597d73906074a9b48cccd/Screenshot%20from%202025-01-30%2017-15-07.png)
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/b5cf657956babe382f2597d73906074a9b48cccd/Screenshot%20from%202025-01-30%2017-15-37.png)

EDITED CONFIG.TCL 
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/b5cf657956babe382f2597d73906074a9b48cccd/Screenshot%20from%202025-01-30%2017-45-53.png)

RUN OPENLANE FLOW SYNTHESIS WITH INSERTED NEWLY CUSTOM INVERTER CELL
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/b5cf657956babe382f2597d73906074a9b48cccd/Screenshot%20from%202025-01-30%2017-52-24.png)
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/b5cf657956babe382f2597d73906074a9b48cccd/Screenshot%20from%202025-01-30%2017-52-33.png)

![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/b5cf657956babe382f2597d73906074a9b48cccd/Screenshot%20from%202025-01-30%2017-54-35.png)

NOTING DOWN CURRENT DESIGN VALUES GENERATED BEFORE MODIFYING PARAMETERS TO IMPROVE TIMING

![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/b5cf657956babe382f2597d73906074a9b48cccd/Screenshot%20from%202025-01-30%2017-56-12.png)
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/b5cf657956babe382f2597d73906074a9b48cccd/Screenshot%20from%202025-01-30%2017-56-26.png)

# Now that we have entered the OpenLANE flow contained docker sub-system we can invoke the OpenLANE flow in the Interactive mode using the following command./flow.tcl -interactive
# Now that OpenLANE flow is open we have to input the required packages for proper functionality of the OpenLANE flowpackage require openlane 0.9
# Now the OpenLANE flow is ready to run any design and initially we have to prep the design creating some necessary files and directories for running a specific design which in our case is 'picorv32a'prep -design picorv32a
# Adiitional commands to include newly added lef to openlane flowset lefs [glob $::env(DESIGN_DIR)/src/*.lef]add_lefs -src $lefs
# Now that the design is prepped and ready, we can run synthesis using following command
run_synthesis

![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/ec26fe25a126546466b0de4f90f7b86fdb73b424/Screenshot%20from%202025-01-30%2018-53-17.png)
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/ec26fe25a126546466b0de4f90f7b86fdb73b424/Screenshot%20from%202025-01-30%2019-41-59.png)

CAMPARING TO PREVIOUSLY NOTED RUN VALUES AREA HAS INCREASED AND WORST NEGATIVE SLACK HAS BECOME 0
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/ec26fe25a126546466b0de4f90f7b86fdb73b424/Screenshot%20from%202025-01-30%2019-42-17.png)
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/ec26fe25a126546466b0de4f90f7b86fdb73b424/Screenshot%20from%202025-01-30%2019-42-36.png)

now THAT OUR CUSTOM INVERTER IS PROPERLY ACCEPTED IN SYNTHESIS WE CAN NOW RUN FLOORPLAN AND PLACEMENT

RUN_SYNTHESIS

SCREENSHOTS OF COMMAND RUN
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/ec26fe25a126546466b0de4f90f7b86fdb73b424/Screenshot%20from%202025-01-30%2019-43-29.png)

since WE HAVE FACED UNEXPECTED ERROR WE USE SET OF COMMANDS AVAILABLE UNDER FLOORPLAN.TCL AND OPENLANE_COMMANDS.MD
init_floorplan
place_io
tap_decap_or

![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/ec26fe25a126546466b0de4f90f7b86fdb73b424/Screenshot%20from%202025-01-30%2019-52-00.png)
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/ec26fe25a126546466b0de4f90f7b86fdb73b424/Screenshot%20from%202025-01-30%2019-52-19.png)
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/ec26fe25a126546466b0de4f90f7b86fdb73b424/Screenshot%20from%202025-01-30%2019-52-38.png)

NOW THAT FLOORPLAN IS DONE WE CAN DO PLACEMENT
RUN_PLACEMENT

![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/ec26fe25a126546466b0de4f90f7b86fdb73b424/Screenshot%20from%202025-01-30%2019-54-17.png)

after placement now command to load placement def in magic in another terminal

![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/ec26fe25a126546466b0de4f90f7b86fdb73b424/Screenshot%20from%202025-01-30%2020-07-14.png)

SCREENSHOT OF PLACEMENT DEF IN MAGIC
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/b3995ab17cda706c4b584b7ad69bcfd4e4b10b73/Screenshot%20from%202025-02-01%2010-40-43.png)

SCREENSHOT OF CUSTOM INVERTER INSERTED IN PLACEMENT DEF 
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/b3995ab17cda706c4b584b7ad69bcfd4e4b10b73/Screenshot%20from%202025-02-01%2010-47-04.png)


pre_sta.conf file for STA in openlane directory
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/c32dd360fbabf9a6a3a518693a9f3632d46821c7/Screenshot%20from%202025-02-02%2014-41-34.png)

my_base.sdc file 
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/fd7a82c0f66325cb1522d7f616da3ef79871b87b/Screenshot%20from%202025-02-02%2014-48-17.png)
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/fd7a82c0f66325cb1522d7f616da3ef79871b87b/Screenshot%20from%202025-02-02%2014-48-28.png)

STA ANALYSIS
SCREENSHOTS OF COMMANDS
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/fd7a82c0f66325cb1522d7f616da3ef79871b87b/Screenshot%20from%202025-02-02%2014-42-41.png)
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/fd7a82c0f66325cb1522d7f616da3ef79871b87b/Screenshot%20from%202025-02-02%2014-42-46.png)
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/fd7a82c0f66325cb1522d7f616da3ef79871b87b/Screenshot%20from%202025-02-02%2014-42-51.png)
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/fd7a82c0f66325cb1522d7f616da3ef79871b87b/Screenshot%20from%202025-02-02%2014-43-02.png)
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/fd7a82c0f66325cb1522d7f616da3ef79871b87b/Screenshot%20from%202025-02-02%2014-43-08.png)
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/fd7a82c0f66325cb1522d7f616da3ef79871b87b/Screenshot%20from%202025-02-02%2014-43-15.png)

COMMANDS LOAD THE DESIGN AND RUN
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/6660b6f059ce4867bcab05d97f48b11ccb1607e8/Screenshot%20from%202025-02-02%2015-44-08.png)
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/ebf458e5cf051644f87d48ecf9007facd4a78bb0/Screenshot%20from%202025-02-02%2015-44-34.png)
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/ebf458e5cf051644f87d48ecf9007facd4a78bb0/Screenshot%20from%202025-02-02%2015-51-08.png)
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/ebf458e5cf051644f87d48ecf9007facd4a78bb0/Screenshot%20from%202025-02-02%2015-52-35.png)
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/ebf458e5cf051644f87d48ecf9007facd4a78bb0/Screenshot%20from%202025-02-02%2015-53-02.png)
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/ebf458e5cf051644f87d48ecf9007facd4a78bb0/Screenshot%20from%202025-02-02%2015-54-43.png)


FINAL STEPS FOR RTL2GDS USING TRITONROUTE AND OPENSTA

PERFORM GENERATION PF POWER DISTRIBUTION NETWORK ANS EXPLORE THE PDN LAYOUT

 Now that we have entered the OpenLANE flow contained docker sub-system we can invoke the OpenLANE flow in the Interactive mode using the following command

./flow.tcl -interactive

 Now that OpenLANE flow is open we have to input the required packages for proper functionality of the OpenLANE flow
 
 package require openlane 0.9
 
 
 Now the OpenLANE flow is ready to run any design and initially we have to prep the design creating some necessary files and directories for running a specific design which in our case is 'picorv32a'

prep -design picorv32a

 Addiitional commands to include newly added lef to openlane flow merged.lefset 

lefs [glob $::env(DESIGN_DIR)/src/*.lef

add_lefs -src $lefs

 Command to set new value for SYNTH_STRATEGY
set ::env(SYNTH_STRATEGY) "DELAY 3"
 
 Command to set new value for SYNTH_SIZING
set ::env(SYNTH_SIZING) 1
 
 Now that the design is prepped and ready, we can run synthesis using following command
run_synthesis

Following commands are alltogather sourced in "run_floorplan" command
init_floorplan
place_io
tap_decap_or

Now we are ready to run placemen
trun_placement

With placement done we are now ready to run CTS
run_cts

Now that CTS is done we can do power distribution network
gen_pdn 

![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/ebf458e5cf051644f87d48ecf9007facd4a78bb0/Screenshot%20from%202025-02-02%2016-20-03.png)

SCREENSHOTS OF PDN DEF

![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/ebf458e5cf051644f87d48ecf9007facd4a78bb0/Screenshot%20from%202025-02-02%2016-18-15.png)
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/ebf458e5cf051644f87d48ecf9007facd4a78bb0/Screenshot%20from%202025-02-02%2016-19-21.png)
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/ebf458e5cf051644f87d48ecf9007facd4a78bb0/Screenshot%20from%202025-02-02%2016-19-34.png)

SCREENSHOTS OF ROUTING RUN

![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/4d0bb3d7477184672560da142930c08f64eeb7d5/Screenshot%20from%202025-02-02%2017-20-08.png)
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/4d0bb3d7477184672560da142930c08f64eeb7d5/Screenshot%20from%202025-02-02%2017-20-16.png)

SCREENSHOT OF ROUTING DEF

![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/4d0bb3d7477184672560da142930c08f64eeb7d5/Screenshot%20from%202025-02-02%2017-23-23.png)
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/4d0bb3d7477184672560da142930c08f64eeb7d5/Screenshot%20from%202025-02-02%2017-23-48.png)
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/4d0bb3d7477184672560da142930c08f64eeb7d5/Screenshot%20from%202025-02-02%2017-26-56.png)
![image_alt](https://github.com/mishika20/Digital-VLSI-Soc-Design-/blob/4d0bb3d7477184672560da142930c08f64eeb7d5/Screenshot%20from%202025-02-02%2017-28-35.png)

