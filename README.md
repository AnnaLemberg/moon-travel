# moon-travel
def calculate_vacation_days(total_days_in_year=365):
    # Input: Number of working days per year
    working_days_per_year = int(input("Enter the number of working days per year: "))

    # Input: Desired travel days per year
    desired_travel_days = int(input("Enter the number of desired travel days per year: "))

    # Input: Desired leisure/vacation days per year
    desired_vacation_days = int(input("Enter the number of desired leisure/vacation days per year: "))

    # Calculate remaining days after work and travel
    remaining_days = total_days_in_year - (working_days_per_year + desired_travel_days + desired_vacation_days)

    # Ensure that remaining days are non-negative
    if remaining_days < 0:
        print("You've allocated more days than available in a year. Please adjust your work, travel, or vacation days.")
    else:
        print(f"Working days per year: {working_days_per_year} days/year")
        print(f"Desired travel days per year: {desired_travel_days} days/year")
        print(f"Desired leisure/vacation days per year: {desired_vacation_days} days/year")
        print(f"Remaining days for other activities: {remaining_days} days/year")

        # Check if the user is satisfied with the balance
        satisfied = input("Are you satisfied with this balance? (yes/no): ").strip().lower()
        if satisfied == "no":
            print("Please re-evaluate your time allocation and adjust accordingly.")
        else:
            print("Great! You have a balanced schedule.")

# Call the function
calculate_vacation_days()
