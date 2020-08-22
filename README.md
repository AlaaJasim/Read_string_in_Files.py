

def function_write(name):

	list_one =  ["Hello" , "from" , "php" ,"course"]

	list_two = []

	for i in range(len(list_one)):
                

		if list_one[i] == "php":

			list_one[i] = "Python"

			list_two.extend(list_one)
			

	print(list_two) ; del list_one[::]

	with open(f"{name}.txt","w") as file:

		content = file.write(repr(list_two))

	return (content)

print(function_write("File Append"))

def function_Read_File(name):

	with open(f"{name}.txt", "r") as my_File:

		content_Read = my_File.read()

	return(content_Read)

print(function_Read_File("File Append"))


def function_Append(name):

	with open(f"{name}.txt", "a") as Append_File:

		content_Append = Append_File.write("\nThe End !")

	return (content_Append)
print(function_Append("File Append"))
