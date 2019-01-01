this is my new file 



----------------UPDATE --------------------------------------------------
update tblMachineParamVals_multival
set FeatureExtent_offsetXvalLeft = (select new_x_left  
                                        from temp_ref_machine
                                           where  temp_ref_machine.id = 
                                                  tblMachineParamVals_multival.id)
                                                                                                                                                      
where machineConfigurationId in ( select machineConfigurationId from temp_ref_machine);

                                                                                                                      