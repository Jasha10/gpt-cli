- [ ] When displaying a code block, don't indent the code by one space (as doing so makes it harder to copy/paste the code).
    For example, here's some output from gptd:
    ```
    The error is because you're trying to access sys.argv[1] but no command line argument was provided. You can add a check to handle this:


     import toml
     import sys

     def parse_toml(file_path):
         with open(file_path, 'r') as file:
             data = toml.load(file)
         return data

     if len(sys.argv) > 1:
         file_path = sys.argv[1]
         data = parse_toml(file_path)
     else:
         print("Please provide a file path.")
    ```
    Note that the python code is indented by 1 space! Don't do this.
