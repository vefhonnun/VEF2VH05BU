### Frágangur

#### Hvernig á að sameina margar CSS skrár í eina skrá

[How to merge multiple files in Python](https://stackoverflow.com/questions/68516922/how-to-merge-multiple-files-in-python)

```python


files_names = [
   "new",
   "grid",
   "table",
   "form",
   "menues",
   "popup",
   "icomoon",
   "chatbox",
   "kvikun",
   "accordion",
   "custom" ]
data = ""

for file_name in files_names :
   with open(file_name+".css" ,"r") as file_handle :
      temp_data = file_handle.read()
      data = data + temp_data 

with open ('styles.min.css', 'w') as file_handle : 
  file_handle.write(data)

```

##### Þjöppun CSS kóða _CSS Compressor_

* Sækið viðbót (Extension) í Visual Studio Code sem heitir "CSS Compressor" 
* Til að þjappa (_Compact_) kóðann saman, notið skipunina: `[shift]+[alt]+[f]`

#### Vefur á Github.io
* [Uppsetning vefs á github.io](../uppsetning-github.io/README.md)

