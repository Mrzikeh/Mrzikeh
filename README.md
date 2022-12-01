- 👋 Hi, I’m @Mrzikeh


options = ["Batu", "Kertas", "Gunting"]
def get_computer_choise(data_options):
	len_options = len(data_options)
	random_data = random.randint(0, len_options-1)
	random_data = data_optionz[random_data]
	return random_data
	
def get_user_choice(data_options):
	is_valid_choice = False
	user_choice = " "
	len_options = len(data_options)
	
	while not is_valid_choice:
		print("Masukkan Pilihan: ")
		for i in range(len_options):
			print(f"#.{data_options[i]}")
			
		user_input = input("Masukkan disini")
		if user_input is not None and user_input in data_options:
			is_valid_choice = True
			user_choice = user_input
			
		if not is_valid_choice:
			print("Anda Harus Masukkan Pilihan Yang Valid Tolol!!!")
			
	return user_choice
	
def print_result(user_choice, computer_choice):
	if user_choice == computer_choice:
		result = "Imbang Bang"
		
	elif user_choice == "Batu" and computer_choice == "Gunting" or user_choice == "Kertas" and computer_choice == "Batu" or user_choice == "Gunting" and computer_choice == "Kertas":
		result = "Anda Menang Bang"
		
	else:
		result = "Anda Kalah Bang"
		
	print(f"Pilihan Anda Adalah {user_choice}. Saya memilih {computer_choice}. {result}")
	
def main():
	computer = get_computer_choice(options)
	user : get_user_choice(options)
	print_result(user, computer)
	
	if __name__ == '__main__' :
		main()
	
