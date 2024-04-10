# Trey Shneour

This is a Github User Page I made for CSE 110 at UCSD. The readme file is [here](README.md) in this Github Repository.

**Table of Contents**
- [Trey Shneour](#trey-shneour)
  - [About Me](#about-me)
  - [Projects](#projects)
  - [Honorable Mention](#honorable-mention)

## About Me

Hello! My name is Trey Shneour and I am a second-year CS major at UCSD. I currently work as a tutor for *CSE 12 - Basic Data Structures and Algorithms* and I am also a researcher in a bioinformatics lab as part of the Early Scholar's Research Program (ESRP for short). 
Some things I am interested in are:
1. Games (Board games, card games, video games)
2. Cats
3. Legos (I own a Lego version of the Daily Bugle from Spiderman which you can see on the [Lego Website](https://www.lego.com/en-us/product/daily-bugle-76178))

## Projects

As mentioned earlier, I am a participant in the ESRP program which aims to introduce CSE undergrads to research. The [ESRP website](https://sites.google.com/ucsd.edu/ersp/home) describes it as such,

> "The UCSD Computer Science and Engineering Early Research Scholars Program (CSE-ERSP) is a team-based research apprentice experience for computer science and engineering majors in their second year of the program."

In my time in the program, I've been able to connect with top researchers alongside the postdocs and grad students working with them. It is a challenging experience which has taught me a lot about research and independently solving problems. Here is some spaghetti code from my project:

```
for index, row in uf_categorized_df.iterrows():

sample = row['sample']
sample_name = re.sub(r'_amplicon\d+_SV_summary.tsv$', "", sample)
#print(sample[0:-25])
#print(code_df.get('name').str.contains(sample[0:-25]))
matching_row = code_df[code_df.get('name').str.contains(sample_name)]

if not matching_row.empty:
    TCGA_code = matching_row['TCGA_code'].values[0]
    TCGA_code = (TCGA_code.split("-"))[1]
    #print(TCGA_code)
    uf_categorized_df.at[index, 'TSS_code'] = TCGA_code
    matching_type = source_df[source_df.get('TSS Code') == TCGA_code]
    uf_categorized_df.at[index, 'cancer_type'] = matching_type['Study Name'].values[0]
    #print(code_df.at[index, 'sample'])
    #print('Success')
elif matching_row.empty:
  print("Didn't find a match")
  # print(sample[0:-25])
```

I also created a game project which I am unable to show here but it is a Space-Invader's esque bullet hell which I made in two weeks with a team of 4 members. Some goals of mine I have are below (some of which are completed).

- [x] Create a game and learn an engine (Unity, Godot, etc.)
- [x] Experiment with Research
- [ ] Create an ML project which aims to compete in a simple game against a player (Wordle, 2048, Chess, etc.)
- [ ] Get an internship
- [ ] Touch grass

## Honorable Mention

![](https://i.pinimg.com/736x/a1/ab/77/a1ab77fb3f301bafd773f3a21e7991a9.jpg)

I really like this image.