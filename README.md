## Advent of Code Template

A template repo for attempting Advent of Code challenges.

This is inspired by [Anthony Sottile's](https://github.com/anthonywritescode/aoc2015) Advent of Code Repo.

This repo provides a template `day00` directory that can be copied for each day's problem.

It also contains a `aoc` module that has a small CLI for downloading inputs and submitting solutions.

The `aoc` module also contains some help functions for solving the problems.

To download inputs and submit solutions just make a copy of the `.env.template` and add your AoC session cookie.

```sh
cp .env.template .env
```

Then install the dependencies, I've used `poetry` to manage the dependencies.

```sh
poetry install
```

## Solving a puzzle

To solve a problem recursively copy the `day00` directory naming the new directory after the day you want to solve.
So for example to solve day 1's problem do the following;

```sh
cp -r day00 day01
cd day01
```

You can download the input for this day by running

```sh
poetry run aoc download-input
```

When you have solved the problem you can submit it by running the following command;

```sh
poetry run python part1.py input.txt | poetry run aoc submit --part 1
```

This will submit part 1 to submit part 2 do the following

```sh
poetry run python part2.py input.txt | poetry run aoc submit --part 2
```
