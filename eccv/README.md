This folder's dataset comprises of 300 government forms and documents in total. 'data.zip' contains 'imgs' and 'jsons' folders.

1. 'img_url_map.json' comprises of a mapping between filename and publicly available url of the pdf which was used to extract the form
2. The 'imgs' folder contains the forms images. 
3. Bounding box annotations of the structures are present in the corresponding json under 'jsons' directory.
4. Given a form, its json is a dictionary comprising of structures' name as keys. The value of each key is a list of bounding boxes for the corresponding structure.
These annotations are present for the following structures (as described and studied in the paper): TextRun, Widget, TextBlock, ChoiceGroupTitle, Field, ChoiceField, ChoiceGroup, Table and List.
