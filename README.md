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
