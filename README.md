# Modeling real systems in Maude: course materials

Materials for the project-based assessment described in

> Adrián Riesco and Juan Rodríguez-Hortalá. *Modeling Real Systems in Maude:
> Making the Declarative Decisions the Assignment.* TFPIE 2027.

In *Auditoría, Calidad y Fiabilidad Informáticas* (master's level,
Universidad Complutense de Madrid), teams of two or three students choose a
real architecture, specify it in Maude, state and verify properties of it,
mutate their own specification to break those properties, and defend the
result individually. Nothing is given: designing the algebra and deciding what
belongs in the equational layer and what in the rule layer are the
assignment.

16 students, an eight-week block, two 100-minute sessions a week. The project
is worth 2.5 of the 10 points of the course.

## Contents

| Folder | What is in it |
|---|---|
| [`practicals/`](practicals/) | The three short, ungraded practicals of the first three weeks (binary search tree, a shop specification to modify, triangular peg solitaire), in Spanish (the originals) and English, with the specification the second one hands out (`tienda.maude`, and `shop.maude` in English). Solutions are not included. |
| [`statement/`](statement/) | The project statement students receive, in Spanish (the original) and English. LaTeX sources and PDF. |
| [`catalogue/`](catalogue/) | The twelve candidate systems with the properties each invites and the team size each is scoped for, and the grading rubric. |
| [`teaching/`](teaching/) | Week-by-week plan, defense logistics, and the repertoire of live modifications asked for in the defense. |
| [`survey/`](survey/) | The end-of-term survey, in Spanish (administered) and English (translation), and a guide to setting it up in Moodle. |
| [`calibration/`](calibration/) | Our own publish-subscribe model, published as an example of a specification that would *not* earn top marks, and why. |
| [`preamble/`](preamble/) | The shared LaTeX preamble the statement and survey need. |

## Building the PDFs

The PDFs are included. To rebuild one, run `pdflatex` from its own folder;
the sources load the preamble from `../preamble/`. The preamble needs
PSTricks (`pst-all`), which is not part of a minimal TeX Live installation
(on Debian and Ubuntu: `texlive-pstricks`), and the Spanish sources need
`texlive-lang-spanish`.

## Maude version

Projects are graded with Maude 3.5. Students may use any version.

## What is not here

Student submissions, and any per-student data.

## License

Documents are licensed under CC BY 4.0, and the Maude code under the MIT
License. See [`LICENSE.md`](LICENSE.md).

## Citation

If you use these materials, please cite the paper above.
