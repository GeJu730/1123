def speed_dial_v1(contact_list):
    sd_name, sd_number, sd_freq = contact_list.pop()
    while len(contact_list) > 0:
        name, number, freq = contact_list.pop()
        if freq > sd_freq:
            sd_name, sd_number, sd_freq = name, number, freq
    return (sd_name, sd_number)

list1 = [('Buffy', '04#', 5),('Blade', '04#', 2),('Abe', '03#', 4)]
x = speed_dial_v1(list1)
list2 = [('Tiffany', '04#', 5),('Hermione', '07#', 2),('Morgan', '00#', 4)]
y = speed_dial_v1(list2)
print(x)
print(y)

def speed_dial_v2(contact_list):
    sd_name, sd_number, sd_freq = contact_list[0]
    for contact in contact_list:
        name, number, freq = contact
        if freq > sd_freq:
            sd_name, sd_number, sd_freq = name, number, freq
    return (sd_name, sd_number)
list1 = [('Buffy', '04#', 4),('Blade', '04#', 2),('Abe', '03#', 4)]
x = speed_dial_v2(list1)
list2 = [('Tiffany', '04#', 5),('Hermione', '07#', 2),('Morgan', '00#', 4)]
y = speed_dial_v2(list2)
print(x)
print(y)
