Documentation for KGCOEReport LaTeX Template
============================================

# General Usage
Stick the `labeport.cls` file in the same folder as the `.tex` document or in your local `texmf` directory and use it as the document class with the department code as an option

```
\documentclass{labreport}
```
# Cover Page Variables
The following is a list of variables used by the template.
Examples are provides in the enclosing brackets.

## Generic Variables
### Required
* `\classCode`: The 4 character code and 3 digit number `[CMPE 160]`
* `\name`: Your name `[Jeff Mahoney]`
* `\LabSectionNum`: The lab section number `[01]`
* `\exerciseNumber`: The exercise number `[1]` or `[One]`
* `\exerciseDescription`: Short description of the exercise. Generally taken
  from the exercise write-up `[Characterizing a OPB745 Sensor]`
* `\dateDone`: The date the lab was performed in ISO 8601 format. If done over
   several lab periods then the first date `[2016-09-19]`
* `\dateSubmitted`: The date the report is due in ISO 8601 format `[2016-09-26]`
* `\LabInstructor`: The name of the instructor for the lab section
  `[Professor Professor]`
* `\TAs`: A list of TA's separated by double backslashes
  `[TA One \\ TA Two \\ TA Three]`
* `\LectureSectionNum`: The lecture section number `[03]`
* `\LectureInstructor`: The name of the instructor for the lecture section
  `[Professor X]`

### Optional
* `\partnerName`: The name of your partner `[Gary Lake]`

#### Sections
Sections are defined by `#`.
There must be a new line, the `#` character, one space,
and then the section name followed by a newline.
Subsections use `##`, subsubsections use `###`.

```
...

# Design Methodology
...

## A Specific Part
...

### Even More Specific
...
```

#### Math Equation
Math equations use the `$` character.
Equations are enclosed in these characters using the
[LaTeX math formatting syntax](https://www.sharelatex.com/learn/Mathematical_expressions)

A single `$` inlines an equation.
There must not be any spaces between the opening `$` and the first character,
and there must not be a space between the last character and the closing `$`

```
... $F = ma$ ...
```

A double `$$` centers the equation and puts it on a new line.
The space requirement is not in effect for this.

```
...
$$ F = -kx $$
...
```

#### Images
Images use the link syntax prepended with a `!`.
The image caption is enclosed within `[]`,
while the image location is enclosed within `()`.

There must be a new line above and below the image line or
Pandoc will attempt to inline the image (and fail).

```
...

![Graph of the waveforms](img/graph.png)

...
