# Test internship

The purpose of this test is to unsure you know:
- basic git knowledge
- basic python programing knowledge
- basic docker knowledge
- basic sql knowledge

To do so, you will resolve a problem running a python command as follows:

`python my-command.py advent-of-code --input-file {path-of-the-file}`

The result must be display in standard output:
Also, it needs to be stored in a postgresql database for log purposes with:
 - execution date of the command
 - the input file path
 - The result of the command

Requisite:
 - You can't use ORM to interact with the database
 - You must use [poetry](https://python-poetry.org/)
 - You must package your command with Docker, one container for the app, the other for the bdd with the command to launch to make it work with docker
 - The small project must be a git repository hosted in github. 


## Stated problem

One Elf has the important job of loading all of the rucksacks with supplies for the jungle journey. Unfortunately, that Elf didn't quite follow the packing instructions, and so a few items now need to be rearranged.

Each rucksack has two large compartments. All items of a given type are meant to go into exactly one of the two compartments. The Elf that did the packing failed to follow this rule for exactly one item type per rucksack.

The Elves have made a list of all of the items currently in each rucksack (your puzzle input), but they need your help finding the errors. Every item type is identified by a single lowercase or uppercase letter (that is, a and A refer to different types of items).

The list of items for each rucksack is given as characters all on a single line. A given rucksack always has the same number of items in each of its two compartments, so the first half of the characters represent items in the first compartment, while the second half of the characters represent items in the second compartment.

For example, suppose you have the following list of contents from six rucksacks:

```text
vJrwpWtwJgWrhcsFMMfFFhFp
jqHRNqRjqzjGDLGLrsFMfFZSrLrFZsSL
PmmdzqPrVvPwwTWBwg
wMqvLMZHhHMvwLHjbvcjnnSBnvTQFn
ttgJtRGJQctTZtZT
CrZsJsPPZsGzwwsLwLmpwMDw
```

- The first rucksack contains the items vJrwpWtwJgWrhcsFMMfFFhFp, which means its first compartment contains the items vJrwpWtwJgWr, while the second compartment contains the items hcsFMMfFFhFp. The only item type that appears in both compartments is lowercase p.
- The second rucksack's compartments contain jqHRNqRjqzjGDLGL and rsFMfFZSrLrFZsSL. The only item type that appears in both compartments is uppercase L.
- The third rucksack's compartments contain PmmdzqPrV and vPwwTWBwg; the only common item type is uppercase P.
- The fourth rucksack's compartments only share item type v.
- The fifth rucksack's compartments only share item type t.
- The sixth rucksack's compartments only share item type s.

To help prioritize item rearrangement, every item type can be converted to a priority:

- Lowercase item types a through z have priorities 1 through 26.
- Uppercase item types A through Z have priorities 27 through 52.

In the above example, the priority of the item type that appears in both compartments of each rucksack is 16 (p), 38 (L), 42 (P), 22 (v), 20 (t), and 19 (s); the sum of these is 157.

Find the item type that appears in both compartments of each rucksack. What is the sum of the priorities of those item types?

The input file is [here](./input_file.txt)

## Extra

This problem is an extract of series of challenges proposed by https://adventofcode.com/.
It's day 3 problem.

If you want to go further, you could add other days and add parameters to the original command such as:

`python my-command.py advent-of-code --input-file {path-of-the-file} --day 1 --part 2`


But this is optional, so do it only if you are having fun solving this kind of problem :)