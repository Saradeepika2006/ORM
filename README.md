# Ex02 Django ORM Web Application
# Date:30-9-2024
# AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

# ENTITY RELATIONSHIP DIAGRAM
## DESIGN STEPS
## STEP 1:
Clone the problem from GitHub

## STEP 2:
Create a new app in Django project

## STEP 3:
Enter the code for admin.py and models.py

## STEP 4:
Execute Django admin and create details for 10 books

# PROGRAM
```# models.py
# Create your models here.
from django.db import models
from django.contrib import admin

class Loan(models.Model):
    loan_id = models.AutoField(primary_key=True)
    customer_name = models.CharField(max_length=100)
    loan_amount = models.DecimalField(max_digits=10, decimal_places=2)
    interest_rate = models.DecimalField(max_digits=5, decimal_places=2)
    loan_term = models.IntegerField()
    disbursement_date = models.DateField()

class LoanAdmin(admin.ModelAdmin):
    list_display=('loan_id','customer_name','loan_amount','interest_rate','loan_term','disbursement_date')
```

```# admin.py
# Register your models here.
from django.contrib import admin

# Register your models here.
from .models import Loan,LoanAdmin

admin.site.register(Loan,LoanAdmin)
```

# OUTPUT
Include the screenshot of your admin page.
![EX 2 TERMINAL](https://github.com/user-attachments/assets/096b5fcb-09a5-4603-bef0-eae53469c8cc)
![EX 2 OUT 1](https://github.com/user-attachments/assets/fd1abcb6-20bf-405f-95b3-12831632197f)
![EX 2 OUT 2](https://github.com/user-attachments/assets/a3b054b8-abdb-49ab-a14b-c8676b517736)
![diagram](https://github.com/user-attachments/assets/660e0979-c5ff-409c-99b4-419c365cc5ab)





# RESULT
Thus the program for creating a database using ORM hass been executed successfully
