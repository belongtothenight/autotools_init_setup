# Compile with AutoTools

## Requirements

1. make
2. libtool
3. automake
4. git

## Commands

### Create configuration from scratch

```bash
touch Makefile.am
```

Fill in your settings to Makefile.am.

```bash
autoscan
mv configure.scan configure.ac
```

Update configure.ac with your settings.

```bash
autoreconf -iv
```

For steps demonstration, see materials 3.

### Go through everything and leave only source code for git upload

autoreconf -iv && ./configure && make && make clean-local

### Development

autoreconf -iv && ./configure && make

make clean && tree . -a

### Prepare for Distribution

autoreconf -iv && ./configure && make tar

Note: This part seems to not be working properly

## Materials

1. [YouTube - autotools](https://www.youtube.com/watch?v=4q_inV9M_us&list=PL02Rn_ZVl7_pB3UzeGhqvbqCQIsnheVzP)
2. [GNU Automake Documentation](https://www.gnu.org/software/automake/manual/1.7.7/automake.html)
3. [YouTube - Creating a simple Autotools based project](https://youtu.be/dc1kEJvS248?si=OZhTi7vqq54PPE_5)
