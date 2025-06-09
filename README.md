# main.py
print("CI/CD процесі сәтті жұмыс істеп тұр!")
name: CI Example

on:
  push:
    branches: [ main ]

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
    - name: Кодты алу
      uses: actions/checkout@v2

    - name: Python орнату
      uses: actions/setup-python@v2
      with:
        python-version: '3.9'

    - name: Кодты тексеру
      run: echo "Код сәтті алынды және тексерілді"

