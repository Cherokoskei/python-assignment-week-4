# python-assignment-week-4
def read_and_modify_file():
    filename = input("Enter the filename to read: ")

  try:
        with open(filename, "r") as file:
            content = file.read()
        
  modified_content = content.upper()  # Example modification
        
  new_filename = "modified_" + filename
        with open(new_filename, "w") as new_file:
            new_file.write(modified_content)

  print(f"Modified content saved to {new_filename}")

  except FileNotFoundError:
        print("Error: File not found. Please check the filename and try again.")
    except IOError:
        print("Error: Could not read the file. Check the file permissions.")

read_and_modify_file()
