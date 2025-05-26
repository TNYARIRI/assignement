
def modify_file_content(input_filename, output_filename):
    try:
        
            lines = file.readlines()

        # Write modified content to a new file
        with open(output_filename, 'w') as new_file:
            for i, line in enumerate(lines, start=1):
                new_file.write(f"{i}: {line}")
        
        print(f"Modified file has been saved as '{output_filename}'.")

    except FileNotFoundError:
        print("Error: The file does not exist.")
    except IOError:
        print("Error: The file could not be read or written.")


filename = input("Enter the name of the file to read: ")
new_filename = "modified_" + filename

modify_file_content(filename, new_filename)
