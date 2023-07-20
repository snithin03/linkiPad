# linkiPad
DevX RUN SEAL JSON Transformer Coding Challenge

Overview:

I developed a Python-based solution that has two key steps:

	1.	Reading the JSON input file and converting it into a Python dictionary.
	2.	Transforming the Python dictionary to align with the required specifications.

I used Python’s built-in json module for parsing the JSON input, and a custom Python function for the transformation.

JSON Parsing:

The first part of the solution involved reading the contents from a JSON input file and storing it as a Python dictionary. 

JSON Transformation:

The second part of the solution involved transforming the Python dictionary. I wrote a recursive Python function, transform_json(data), that traverses the dictionary and performs the required transformations. 

 In this function:

	•	I initialize an empty dictionary, result, to hold our transformed data.
	•	I then loop over each key-value pair in the input dictionary, data.
	•	If the value is a dictionary (i.e., a nested JSON object), I recursively call transform_json on the value to transform it as well.
	•	I then check if the key is already in result:
	•	If it is, I check if the existing value for this key is a list. If it is, I append the new value to the list. If it’s not, I create a new list containing the 
    existing value and the new value.
	•	If the key is not in result, I add the key-value pair to result as is.

Usage:

To utilize these functions, update the value of 'file_path' in main.py. 

This solution should work for most valid JSON inputs. However, I made an assumption that no lists are present in the input JSON, as per the provided json. If our actual data could contain lists, we have to modify the `transform_json` function to handle them properly.
