create wind files for delft3d SWAN module.

Just download the notebook, place it on your env folder alongside your nc and txt files and replace file_paths from the notebook with your file_paths.

Case_02.mdw is a wave file executable by delft3d_wave module. Please download it and check it out. The following lines of the file are very important for varying space/time wind file and you should copy and paste them into your wind file.

   MeteoFile            = xwind.wnd    
   
   MeteoFile            = ywind.wnd 

   DirConvention        = cartesian

   this cartesian coordinate shouldn't be misunderstood with grid coordinates. It is related to the wind direction and it just means that postive x values are eastward and positive y values are northward. it simply says which direction wind travels. in nautical coordinates, things are reversed and positive values illustrate where wind is coming from. So for the sake of everything to work correctly, keep it cartesian. 
   
