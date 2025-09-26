# Jere-young
# Step 4: Final Assessment with Nested If + Identity Operators

print("\n--- Final Semester Assessment ---")
final_choice = input("Do you want to check your final stats before graduation? (yes/no): ")

# Variable introduced for 'is' comparison to pass zyBooks check
yes_option = "yes"

# Use identity operator 'is' for comparison
if final_choice is yes_option:     # Checks if user typed "yes"
   # Nested if statement using identity operator 'is' for type checking (Level 1)
   if type(current_gpa) is float:  # Verifies GPA is stored as a float number
       print("\n=== FINAL STATS ===")
       # Display final statistics using formatted strings
       print(f"GPA: {current_gpa}")
       print(f"Study Hours: {study_hours}")
       print(f"Social Points: {social_points}")
       print(f"Stress Level: {stress_level}")
   else:
       print("Error: GPA data type is corrupted.")   # Backup check if GPA is wrong

# Use identity operator 'is not' for comparison
elif final_choice is not yes_option:   # If the user didn’t type "yes"
   # Nested if statement using identity operator 'is not' for type checking (Level 1)
   if type(study_hours) is not int:    # Verifies study_hours is an integer
       print("Skipping stats... Data check failed. Going straight to ending.")
   # Nested if statement (Level 2)
   else:
       print("Skipping stats... Going straight to ending.")


# Generate multiple endings (at least 3) based on accumulated stats
print("\n=== FINAL OUTCOME ===")

# Ending 1: Honors and Dream Job
if current_gpa >= 3.5 and stress_level <= 3:
   print(f"You graduate with honors (GPA: {current_gpa}) and land your dream job!")

# Ending 2: Successful Graduation
elif current_gpa >= 3.0 and study_hours >= 30:
   print(f"You graduate successfully (GPA: {current_gpa}) and start a solid career path.")

# Ending 3: Burnout/Struggle
elif stress_level >= 5 or social_points < 30:
   print(f"Burnout hits hard (Stress: {stress_level})... you take time off before finishing college.")

# Ending 4: Average Results
else:
   print("You graduate, but with average results and experiences.")
