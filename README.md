print("======== MAXIM TAXEE BOOKING SYSTEM! ========")

BASE_FARE = 50
PRICE_PER_KM = 20

booking = []
passengers = []

def welcome():
    print("==========================================")
    print("======== WELCOME TO MAXIM TAXEE! =========")
    print("==========================================")
    print("Your ride, your destination!")
    print("safe and convenient transportation.")

print("=============== MAIN MENU ================")

def main_menu():
    print("\n============ MAIN MENU =============")
    print("[1] Passenger Registration")
    print("[2] Booking a Taxee")
    print("[3] View Booking History")
    print("[4] Cancel Booking")
    print("[5] Exit Program")

print("======== PASSENGER REGISTRATION ==========")

def passenger_registration():
    print("\n===== PASSENGER REGISTRATION =======")

    name = input("Enter your Full Name: ")
    contact = input("Enter your Contact Number: ")

    if name == "" or contact == "":
        print("Please Complete all Information.")
        exit() 

    passenger = {"name": name, "contact": contact }

    passengers.append(passenger)

    print("\nRegistration, Successful!")
    print("Passenger Name:", name)
    print("Contact Number:", contact)

print("==========================================")
print("============ BOOKING A TAXEE =============")
print("==========================================")

def booking_taxee():
    print("\n===== PASSENGER REGISTRATION =======")

    if len(passengers) == 0:
        print("Please Register First.")
        exit() 

    name = input("Enter Registered Passenger Name: ")
    passenger_fount = None

    for passenger in passengers:
        if passenger["name"].lower() == name.lower():
            passenger_fount = passenger
            break

    if passenger_fount is None:
        print("passenger not found. Please register.")
        exit() 

print("\n========== TRAVEL INFORMATION =========")

pickup = input("Enter Pickup Location: ")
dropoff = input("Enter dropoff Location: ")

if pickup == "" or dropoff == "":
    print("Pickup Location and dropoff are required.")

try:
    distance = float(input("Enter Distance: "))

    if distance <= 0:
        print("Distance must be greater than zero.")

except ValueError:
    print("Invalid distance. Please enter a number.")

print("==========================================")
print("============ FARE CALCULATION ============")
print("==========================================")

distance_fare = distance * PRICE_PER_KM
total_fare = BASE_FARE + distance_fare

print("\n============= FARE DETAILS =============")
print("Base Fare: PHP", BASE_FARE)
print("Distance: PHP", distance, "km")
print("Price per KM: PHP", PRICE_PER_KM)
print("Distance Fare: PHP", distance_fare,)
print("Total Fare: PHP", total_fare)

print("==========================================")
print("========= BOOKING CONFIRRMATION ==========")
print("==========================================")

confirm = input("\nConfirm your Booking? (y/n): ")
if confirm.lower() != "y":
    exit()

print("==========================================")
print("================ PAYMENT =================")
print("==========================================")

payment = float(input("Enter Payment Amount: "))

if payment < total_fare:
    print("insufficent Payment!")
    print("Booking Was not Completed.")
    print("Invalid Payment Amount.")

    change = payment - total_fare

print("========= MAXIM BOOKING RECEIPT ==========")

print("Base Fare: PHP", BASE_FARE)
print("Distance: PHP", distance, "km")
print("Price per KM: PHP", PRICE_PER_KM)
print("Distance Fare: PHP", distance_fare,)
print("Total Fare: PHP", total_fare)

print("Booking Status: CONFIRMED")
print("Thankyou for choosing Maxim!")

print("============ BOOKING HISTORY =============")

def booking_history():
    print("\n========== BOOKING HISTORY ==========")

    if len(booking_history) == 0:
        print("Please Book First.")
        exit()

    booking_history()

number = int(input("\nBooking History Number: "))


if number < 1 or number > len(booking_history):

    print("This Booking number.")
    exit()

    select_booking = booking[number-1]

if select_booking["status"] == "CANCELED":
    print("This Booking is already Canceled!")
    exit()

booking["statust"] = "canceled"
print("\nBooking successfully Canceled!.")

print("passenger:", select_booking["passenger"])
print("pickup:", select_booking["pickup"])
print("dropoff:", select_booking["dropoff"])
print("status: Canceled")

print("Please enter a valid booking number.")

print("==========================================")
print("       THANK YOU FOR USING MAXIM!         ")
print("          HAVE A SAFE JOURNEY!            ")
print("==========================================")

print("============== MAIN SYSTEM ===============")

welcome()

while True:

    main_menu()

    choice = input("\nEnter your Choice (1-5): ")

    if choice == "1":
        passenger_registration()

    elif choice == "2":
        booking_taxee()

    elif choice == "3":
        booking_history()

    elif choice == "4":
        booking()

    elif choice == "5":
        print("Thankyou for choosing taxee/Maxim!")
        break

    else:
        print("Invalid Choice!")
        print("Please select from 1 to 5.")
        exit() 
