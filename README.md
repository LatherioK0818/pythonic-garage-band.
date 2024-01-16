# LAB - Class 04

Project: Pythonix Garage Band
Author: Latherio Kidd

## Links and Resources

- My back-end server URL (when applicable)
- My front-end application (when applicable)

## Overview

In this project, I've created a simulation of a garage band using Object-Oriented Programming in Python. It includes classes for various types of musicians like Guitarists, Bassists, and Drummers, and a Band class to group these musicians together.

### Features

- I've implemented functionality to read band data from a file.
- I create musician and band objects dynamically.
- The program simulates playing solos for each band member.

## Setup

### Environment Requirements

- `.env` requirements (where applicable)

### Running the Application

To run the application, I use the following command:

```bash
python main.py
```

### How to Use

1. I place the band data in `band.txt`.
2. My program reads this file and creates a band instance with musicians based on the data.
3. Users can simulate the band playing solos and list all the bands created.

## Code Snippet

```python
# Here's a snippet for reading data and creating band instances
def read_file(file):
    ...

# The rest of my code...

# Creating a band instance from data
band_data = read_file("band.txt")
band_data_formatted = Band.create_from_data(band_data)
new_band = Band(band_data_formatted[0], band_data_formatted[1])

# Example of how to use it
print('\n'+ repr(new_band.members) + '\n')
print(str(new_band) + '\n')
print(new_band.play_solos() + '\n')
print(Band.to_list(), '\n')
```

### Tests

#### Running Tests

To run the tests, I use the following command:

```bash
python -m pytest
```

This command executes all the test cases I've defined in the test suite.

#### Notable Tests

My test suite includes several key tests to ensure the correct functionality of the Musician classes (`Guitarist`, `Bassist`, `Drummer`) and the `Band` class. These tests check:

- The role and instrument of each musician type.
- The correct string representation (`__str__`) and formal representation (`__repr__`) of each musician.
- The ability of each musician to play a solo.
- The correct formation and behavior of a band, including playing solos and string representation.
- The functionality to read band data from a file and create a band instance.

#### Specific Test Examples

Here are some examples of the tests I've implemented:

1. `test_guitarist_role`: Verifies the role of a guitarist.
2. `test_guitarist_instrument`: Checks the instrument assigned to a guitarist.
3. `test_guitarist_play_solo`: Ensures a guitarist can play a solo.
4. `test_Band_instance`: Confirms that a band instance is created correctly with the name "Random Group".
5. `test_Band_play_solos`: Tests the play_solos method for the band.
6. `test_Band_to_list`: Verifies that the to_list class method returns all created band instances.

#### Edge Cases

- `test_role_doesn_exist`: Tests the scenario where a given role from the data does not have a corresponding class.
