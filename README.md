Instant Labelling tool. Things that need done: 
- Fix the bbox normalization in sam3_auto_label: it is writing tensors to the output txts instead of float values 
- Add batch inference - it is processing one image at a time 
- The loop in single_image_inference is wrong: it is writing n tensor boxes to the image, and only one normalized 
bbox coordinate. Needs to be all bbox coordinates. 
- Loop in single_image_inference needs to not have duplicates in the bbox coordinates
