This folder contains data of 100 forms. 'data.zip' contains 'imgs' and 'jsons' folders.

1. img_url_map.json comprises of a mapping between filename and publicly available url of the pdf which was used to extract the form
2. 'imgs' folder comprises of the images of the forms.
3. 'jsons' folder comprises of bounding box annotation of each structure (TextRun, Widget, TextBlock, Field, Choice Field and Choice Group) described and studied in the paper.
    1. Given a form, its json comprises of structure name as key and list of instances of each structure as its value
    2. In addition to bounding box, each structure instance is identified by a unique 'structure_id', contains 'text' (in case of TextRuns)
    3. Further, each structure instance contains an optional 'parent_\<structure_name\>' id which can be used to determine association with higher order structure it is part of. For example, each textrun contains id of the parent textblock in which it is contained. Similarly, textblock which is part of a field will have the corresponding 'parent_field' id.
    4. If value of a particular 'parent_id' is not present or null, that means either it is not required by the model (as in paper) or the lower order element is not associated to a higher order structure.
    5. 'Field' refers to text fields and 'Choice_Field' are the boolean fields as discussed in the paper.


Please cite our paper ([Paper link](https://openaccess.thecvf.com/content_WACV_2020/html/Aggarwal_Multi-Modal_Association_based_Grouping_for_Form_Structure_Extraction_WACV_2020_paper.html)) if you use data in this directory:

```js
{
  @inproceedings{aggarwal2020multi,
  title={Multi-Modal Association based Grouping for Form Structure Extraction},
  author={Aggarwal, Milan and Sarkar, Mausoom and Gupta, Hiresh and Krishnamurthy, Balaji},
  booktitle={The IEEE Winter Conference on Applications of Computer Vision},
  pages={2075--2084},
  year={2020}
}
```
