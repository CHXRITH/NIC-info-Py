def parse_nic(nic_no):
    error = ""
    gender = ""
    bday = ""

    if len(nic_no) != 10 and len(nic_no) != 12:
        error = "Invalid NIC NO"
    elif len(nic_no) == 10 and not nic_no[:9].isdigit():
        error = "Invalid NIC NO"
    else:
        # Year
        if len(nic_no) == 10:
            year = "19" + nic_no[:2]
            day_text = int(nic_no[2:5])
        else:
            year = nic_no[:4]
            day_text = int(nic_no[4:7])

        # Gender
        if day_text > 500:
            gender = "Female"
            day_text -= 500
        else:
            gender = "Male"

        # Day Digit Validation
        if day_text < 1 or day_text > 366:
            error = "Invalid NIC NO"
        else:
            # Month
            if day_text > 335:
                day = day_text - 335
                month = "December"
            elif day_text > 305:
                day = day_text - 305
                month = "November"
            elif day_text > 274:
                day = day_text - 274
                month = "October"
            elif day_text > 244:
                day = day_text - 244
                month = "September"
            elif day_text > 213:
                day = day_text - 213
                month = "August"
            elif day_text > 182:
                day = day_text - 182
                month = "July"
            elif day_text > 152:
                day = day_text - 152
                month = "June"
            elif day_text > 121:
                day = day_text - 121
                month = "May"
            elif day_text > 91:
                day = day_text - 91
                month = "April"
            elif day_text > 60:
                day = day_text - 60
                month = "March"
            elif day_text < 32:
                month = "January"
                day = day_text
            elif day_text > 31:
                day = day_text - 31
                month = "February"

    # Show Details
    gender = "Gender: " + gender
    bday = "Birth Date: {} {} {}".format(year, month, day)


    return error, gender, bday


# Example usage:
nic_number = input("Enter NIC number: ")
error, gender, bday = parse_nic(nic_number)

if error:
    print(error)
else:
    print(gender)
    print(bday)
