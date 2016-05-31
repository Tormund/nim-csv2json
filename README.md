About
=====

nim-csv2json is a Nim module for converting data from CSV into its JSON representation.

For the purposes of an example, assume a file called "example.csv" exists and contains
the following data:

    This,is,a
    test,1,2
    3,hello,world

Example:
    
    # Get the CSV data.
    var csv : string = readFile("example.csv")
    
    # Convert the data to a JSON string representation.
    var jsonOutput : string = toJSONString(csv, "", separator = ",")
    # jsonOutput is now set to the following string:
    # {"data": [
    #     ["This", "is", "a"],
    #     ["test", "1", "2"],
    #     ["3", "hello", "world"]
    # ]}
    
    # We could also use toJSON() instead, to return the CSV data represented as
    # a JsonNode.

License
=======

nim-csv2json is released under the MIT open source license.
