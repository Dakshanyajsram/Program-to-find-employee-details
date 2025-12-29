# Program-to-find-employee-details

def get_employee_details():
    name = input("Enter Employee Name: ")
    emp_id = input("Enter Employee ID: ")
    department = input("Enter Department: ")
    basic_salary = float(input("Enter Basic Salary: "))
    return name, emp_id, department, basic_salary
def calculate_salary(basic_salary):
    hra = basic_salary * 0.20     # 20% House Rent Allowance
    da = basic_salary * 0.10      # 10% Dearness Allowance
    pf = basic_salary * 0.12      # 12% Provident Fund deduction
    gross_salary = basic_salary + hra + da
    net_salary = gross_salary - pf
    return hra, da, pf, gross_salary, net_salary
def print_salary_slip(name, emp_id, department, basic, hra, da, pf, gross, net):
    print("\n============== EMPLOYEE SALARY SLIP ==============")
    print("Employee Name   :", name)
    print("Employee ID     :", emp_id)
    print("Department      :", department)
    print("-----------------------------------------------")
    print("Basic Salary    : Rs.", basic)
    print("HRA (20%)       : Rs.", hra)
    print("DA (10%)        : Rs.", da)
    print("PF Deduction    : Rs.", pf)
    print("-----------------------------------------------")
    print("Gross Salary    : Rs.", gross)
    print("Net Salary      : Rs.", net)
    print("================================================")
name, emp_id, department, basic = get_employee_details()
hra, da, pf, gross, net = calculate_salary(basic)
print_salary_slip(name, emp_id, department, basic, hra, da, pf, gross, net)


OUTPUT:
Enter Employee Name: DAKSHANYA
Enter Employee ID: 017
Enter Department: COMPUTER SCIENCE
Enter Basic Salary: 400000

============== EMPLOYEE SALARY SLIP ==============
Employee Name   : DAKSHANYA
Employee ID     : 017
Department      : COMPUTER SCIENCE
-----------------------------------------------
Basic Salary    : Rs. 400000.0
HRA (20%)       : Rs. 80000.0
DA (10%)        : Rs. 40000.0
PF Deduction    : Rs. 48000.0
-----------------------------------------------
Gross Salary    : Rs. 520000.0
Net Salary      : Rs. 472000.0
================================================
