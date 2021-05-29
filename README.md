## Generating Test Data using Faker Module.
Faker is a module for generating fake data, helpful when writing unit test cases or performing some file transfers in case of data engineering when you want to test drive what size can be easily transferred and where does the need arises to chunk. Faker does a great job in creating the sample csv files with ease.

Had to set up some fake data to test the file transfer and the upper limits in terms of the size of file which could be transferred. This required some csv files of varying size to be generated. As we would be generating the CSV file we would inmport csv module into our test.py python file along with faker library. Create a new Faker object. RECORD_COUNT is a constant which can be changed to adjust the size of the file.

## Setting up the Dev Environment
**VSCODE** is the development tool used, have python installed, I have python 3.8.
You could set up your project directory with git or simply clone the repository.
- Set up your project directory
  `cd <localdir>`
- Initialize as a git repository
  `git init`
- Stage the changes
  `git add -A && git commit -m 'initialize'`
- Set up your remote repository in github and provide the url
  `git remote add origin <url>`
- Push to your remote repository
  `git push -u origin master`

You could also clone the repository in your project directory
- Clone the repository into your project directory 
  `git clone https://github.com/mdsabz/faker.git`
- Open up a command Python Terminal (Ctrl+Shift+P, Python: Terminal)
- Set up a virtual environment by specifying the command
`python -m venv venv`

### Installation
  pip install faker

### Basic Usage

  ```
   from faker import Faker
   faker = Faker()
   writer.writerow(
                {
                    'first_name': fake.name(),
                    'last_name': fake.name(),
                    'email': fake.email(),
                    'product_id': fake.random_int(min=100, max=199),
                    'qty': fake.random_int(min=1, max=9),
                    'amount': float(Decimal(random.randrange(500, 10000))/100),
                    'description': fake.sentence(),
                    'address': fake.street_address(),
                    'city': fake.city(),
                    'state': fake.state(),
                    'country': fake.country()
                }
            )
  ```
  Variable **RANDOM_COUNT** determines the number of records which needs to be created.

## References
For Detailed explanation visit: [towardsdatascience](https://towardsdatascience.com/generation-of-large-csv-data-using-python-faker-8cfcbedca7a7)
