# Learning-stage expansion: foundations and training — 2026-10-11

This record covers prerequisite bridges and deeper study, checked against every current `resources/*.md` page before selection. Entries are proposed for the catalog; this record is not itself a second recommendation list. The related [study stages](../study-stages.md) are editorial guidance rather than prerequisites certified by the resource providers.

Only resource-owner, university, author, and official repository pages support the decisions below. Content and access were checked on 2026-10-11. Reading a lesson, finding an exercise, or inspecting a repository does not establish that its code or interactive component was run.

## Selection decisions

The three programming entries have different jobs: a first programming lesson, a focused array reference, and a broader numerical-computing bridge. They are not three separate recommendations for the same package. Companion lessons, documentation, and book drafts remain under their parent resources.

| Resource | Suggested stage | Suggested placement | Distinct gap |
| --- | --- | --- | --- |
| Software Carpentry: Programming with Python | 1 · Build foundations | Foundations / Programming and scientific computing | Programming for readers who cannot yet modify a tutorial. |
| NumPy: the absolute basics for beginners | 1 · Build foundations | Foundations / Programming and scientific computing | Array shapes, indexing, and operations used throughout neuroscience notebooks. |
| Scientific Python Lectures | 1–2 · Foundations to independent practice | Foundations / Programming and scientific computing | Moving from basic code to numerical routines and diagnostics. |
| Interactive Linear Algebra | 1 · Build foundations | Foundations / Mathematical foundations | Visual exploration alongside the existing lecture and reference choices. |
| Biophysics: Searching for Principles | 3–4 · Research to methods | Foundations / Advanced theory | Physical limits, noise, robustness, and information as quantitative research questions. |
| Neuroscience Online | 1–2 · Foundations to independent practice | Foundations / Biological background | A chapter-level biological reference to accompany neuron models. |
| MBL Methods in Computational Neuroscience | 3–4 · Research to methods | Community / Standards, training, and technical help | Intensive training that connects experimental and theoretical perspectives. |

## Accepted evidence and ready entries

### Software Carpentry: Programming with Python

- Canonical URL: [Programming with Python](https://swcarpentry.github.io/python-novice-inflammation/).
- Prerequisites: The lesson explicitly asks for file/directory familiarity and the ability to start a Python interpreter; it targets novice programmers. All lesson episodes belong to this one entry.
- Verified content: The [official lesson](https://swcarpentry.github.io/python-novice-inflammation/) and [source repository](https://github.com/swcarpentry/python-novice-inflammation) cover tabular data, plotting, loops, functions, errors, defensive programming, debugging, and command-line programs. The example uses simulated inflammation data, not neural recordings.
- Access and maintenance: Free online materials and example data. The official GitHub API reported `archived: false` and `disabled: false` for [the repository](https://api.github.com/repos/swcarpentry/python-novice-inflammation). No installation, exercises, or code were run.
- Suggested outcome: Load one supplied table, compute a column summary, plot it, and move the repeated steps into a function. This is an editorial exercise, not a reported result.

Ready entry:

- [Software Carpentry: Programming with Python](https://swcarpentry.github.io/python-novice-inflammation/) - A first programming course built around tabular data, introducing variables, arrays, plotting, loops, functions, debugging, and defensive programming. Useful before neuroscience notebooks that assume basic coding fluency. Free lessons and example data; requires familiarity with files and directories and a working Python interpreter.

### NumPy: the absolute basics for beginners

- Canonical URL: [NumPy beginner guide](https://numpy.org/doc/stable/user/absolute_beginners.html).
- Prerequisites: Editorial recommendation: basic Python variables, lists, indexing, and function calls. A NumPy installation is needed to run local examples.
- Verified content: The [official guide](https://numpy.org/doc/stable/user/absolute_beginners.html) introduces arrays, dimensions, shapes, data types, slicing, copies versus views, reshaping, aggregation, broadcasting, and saving/loading. These address concrete sources of mistakes when manipulating trial-by-neuron or time-by-channel arrays.
- Access and maintenance: Free documentation. The [official repository](https://github.com/numpy/numpy) links the documentation; its [GitHub API record](https://api.github.com/repos/numpy/numpy) returned `archived: false` and `disabled: false`. No examples were executed and no package compatibility claim is made.
- Suggested outcome: Explain each axis of a small trial-by-neuron array and predict the shape after slicing, averaging, and broadcasting.

Ready entry:

- [NumPy: the absolute basics for beginners](https://numpy.org/doc/stable/user/absolute_beginners.html) - The official introduction to numerical arrays covers shapes, data types, indexing, reshaping, aggregation, broadcasting, and copies versus views. Useful for understanding the trial, neuron, and time dimensions in neuroscience notebooks. Free documentation with examples; start after learning basic Python syntax and lists.

### Scientific Python Lectures

- Canonical URL: [Scientific Python Lectures](https://lectures.scientific-python.org/).
- Prerequisites: Editorial recommendation: begin after a first Python lesson; use linear algebra and calculus alongside relevant numerical chapters. The curriculum offers introductory through advanced sections rather than a single formal prerequisite level.
- Verified content: The [contents](https://lectures.scientific-python.org/) connect Python, NumPy, plotting, debugging, sparse arrays, and optimization. The [SciPy chapter](https://lectures.scientific-python.org/intro/scipy/index.html) includes worked examples of interpolation, curve fitting, integration, initial-value ODEs, and Fourier transforms. This provides a bridge to implementing models rather than another neuroscience survey.
- Access and maintenance: Free online chapters and examples. The [about page](https://lectures.scientific-python.org/about.html) documents contributions and environments. The [source repository](https://github.com/scipy-lectures/scientific-python-lectures) and its [API record](https://api.github.com/repos/scipy-lectures/scientific-python-lectures) were checked; `archived` and `disabled` were both `false`. No environment or numerical example was run.
- Suggested outcome: Work through one initial-value example, change its initial condition, and compare the numerical trajectory with a known limiting case.

Ready entry:

- [Scientific Python Lectures](https://lectures.scientific-python.org/) - A progressive guide to Python, numerical arrays, plotting, SciPy, debugging, and optimization, with worked examples of interpolation, curve fitting, differential equations, and Fourier transforms. Useful when moving from following neuroscience notebooks to implementing numerical models. Free online chapters and exercises; basic Python helps with the numerical sections.

### Interactive Linear Algebra

- Canonical URL: [Interactive Linear Algebra](https://textbooks.math.gatech.edu/ila/).
- Prerequisites: Editorial recommendation: algebraic equations and basic coordinate geometry. No calculus prerequisite was asserted by the inspected overview.
- Verified content: The [university-hosted contents](https://textbooks.math.gatech.edu/ila/) cover linear systems, vector spaces, transformations, eigenvalues, orthogonality, and least squares. The [authors' overview](https://textbooks.math.gatech.edu/ila/overview.html) explains the geometric emphasis and interactive demonstrations. Its role differs from the catalog's MIT lecture sequence: it provides manipulable illustrations for difficult concepts.
- Access and verification: Free online text by Dan Margalit and Joseph Rabinoff. The overview and contents were opened; interactive controls were not exercised, and no problem solutions were evaluated.
- Suggested outcome: Relate a displayed eigenvector to a matrix transformation, then explain a least-squares projection geometrically.

Ready entry:

- [Interactive Linear Algebra](https://textbooks.math.gatech.edu/ila/) - An open textbook by Dan Margalit and Joseph Rabinoff combines linear systems, vector spaces, transformations, eigenvalues, orthogonality, and least squares with interactive geometric demonstrations. Useful for building intuition before population models or dimensionality reduction. Free university-hosted text; begin with algebra and coordinate geometry.

### Biophysics: Searching for Principles

- Canonical URL: [William Bialek's book page](https://www.princeton.edu/~wbialek/biophysbook.html).
- Prerequisites: Advanced physics and mathematical maturity. The [author's course description](https://www.princeton.edu/~wbialek/PHY562/home) targets physics PhD students with substantial undergraduate preparation; the [university book record](https://collaborate.princeton.edu/en/publications/biophysics-searching-for-principles-2/) identifies statistical mechanics and quantum mechanics among its tools.
- Verified content: The university record and [author-posted draft contents](https://www.princeton.edu/~wbialek/PHY562.html) connect photon counting, noise, robustness without precise parameter tuning, and efficient information representation to sensory systems and other biological phenomena. This is a research-level conceptual bridge, not a first neuroscience textbook.
- Access and verification: The author page provides problem data; the 2011 draft page links a free prepublication text with explicitly unfinished sections. The published book is a separate edition; use purchase or library access for that edition. The publisher page could not be fetched by the web reader. The linked full draft PDF exceeded the reader's size limit (about 33.9 MB), so only the accessible pages and contents were inspected; the book was not read in full and exercises were not run.
- Suggested outcome: Derive a simple noise-limited measurement prediction and state which biological assumptions would make the bound relevant.

Ready entry:

- [Biophysics: Searching for Principles](https://www.princeton.edu/~wbialek/biophysbook.html) - William Bialek develops quantitative questions about sensory precision, biological noise, robustness, and information representation using physical principles and worked problems. Suited to readers with substantial physics and mathematics. The author provides problem data and a [2011 prepublication draft](https://www.princeton.edu/~wbialek/PHY562.html); the published edition requires purchase or library access.

### Neuroscience Online

- Canonical URL: [Neuroscience Online](https://nba.uth.tmc.edu/neuroscience/).
- Prerequisites: No formal requirement was found on the inspected pages. Editorial recommendation: basic cell biology and selective reading alongside computational coursework rather than completing the whole text first.
- Verified content: The [official university resource page](https://med.uth.edu/nba/resources/neuroscience-online/) identifies an open-access educational resource. The [textbook contents](https://nba.uth.tmc.edu/neuroscience/m/index.htm) list membrane and action potentials, synaptic transmission, plasticity, sensory and motor systems, and higher brain functions. This supplies mechanisms and terminology behind model variables, beyond the existing short Brain Facts primer.
- Access and verification: Free online textbook by UTHealth Houston faculty. Landing page and contents opened in the web reader; a separate programmatic request to the landing page returned HTTP 403. This is not evidence that the textbook requires payment. Interactive components and chapter exercises were not run.
- Suggested outcome: Explain how membrane potential, conductance, and synaptic input in a chosen neuron model correspond to the biological mechanisms described in a selected chapter.

Ready entry:

- [Neuroscience Online](https://nba.uth.tmc.edu/neuroscience/) - An open-access textbook from UTHealth Houston faculty covering cellular and molecular neuroscience, sensory and motor systems, and higher brain functions. Use selected chapters on membrane potentials, synaptic transmission, and plasticity to connect mathematical neuron models with their biological mechanisms. Best used as a foundational reference alongside computational coursework.

### MBL Methods in Computational Neuroscience

- Canonical URL: [Methods in Computational Neuroscience](https://www.mbl.edu/education/advanced-research-training-courses/course-offerings/methods-computational-neuroscience).
- Prerequisites: The [official course page](https://www.mbl.edu/education/advanced-research-training-courses/course-offerings/methods-computational-neuroscience) targets graduate students, postdocs, and faculty with a strong background in one discipline and some preparation in a complementary discipline. Admission is selective.
- Verified content: The first three weeks progress through cellular, network, and cognitive/behavioral material with quantitative exercises; a final week is reserved for research projects. This connects modeling with experimental questions rather than providing another introductory coursebook.
- Access and dates: The [financial-support page](https://www.mbl.edu/education/advanced-research-training-courses/course-offerings/methods-computational-neuroscience/financial-and-course-support) lists tuition and room/board charges plus need-based aid. The course page still lists the completed 2026 cycle (July 24–August 21, application deadline March 22); no future admission opening is claimed. The official [lecture archive](https://www.mbl.edu/education/advanced-research-training-courses/course-offerings/methods-computational-neuroscience/lecture-videos) links recordings from several prior years.
- Verification boundary: Course, fees, and archive entrance were inspected. No application was submitted, and recordings were not individually played or checked for login requirements. The residential course is not described as free.
- Suggested outcome: Identify a course lecture or project topic that connects a current research question to a complementary experimental or theoretical method.

Ready entry:

- [MBL Methods in Computational Neuroscience](https://www.mbl.edu/education/advanced-research-training-courses/course-offerings/methods-computational-neuroscience) - An intensive, selective summer course connecting mathematical models with experimental neuroscience across cellular, circuit, and behavioral scales. Lectures, quantitative exercises, and a research project suit graduate students and researchers with a strong disciplinary background. An official lecture archive supports further study; residential attendance requires an application and fees, with financial aid available.

## Companion improvement, not an additional resource

[Neuromatch's Modeling Step-by-Step Guide](https://compneuro.neuromatch.io/projects/modelingsteps/intro.html) belongs to the existing Neuromatch Computational Neuroscience entry. Its [steps 1–4](https://compneuro.neuromatch.io/projects/modelingsteps/ModelingSteps_1through4.html) connect a phenomenon and question to background reading, model ingredients, and explicit hypotheses. Recommend it at stages 2–3 for readers choosing their own project. The pages were read; notebook widgets and external feedback tools were not run.

Suggested companion clause for the existing entry: `Includes a [modeling project guide](https://compneuro.neuromatch.io/projects/modelingsteps/intro.html) for turning a question into model ingredients and explicit hypotheses.`

## Deferred or rejected candidates

| Candidate | Decision and reason |
| --- | --- |
| A separate NumPy quickstart or MATLAB-migration entry | Defer. Both are linked from the [beginner guide's navigation](https://numpy.org/doc/stable/user/absolute_beginners.html) and belong to the same official documentation ecosystem. Keep one canonical NumPy learning entrance. |
| Separate SciPy, Matplotlib, and general Python software entries | Defer. The [Scientific Python Lectures](https://lectures.scientific-python.org/) already teach the required numerical workflow. Listing every dependency would expand the software inventory without addressing a distinct learning gap. |
| Neuromatch Modeling Step-by-Step Guide as an independent resource | Reject as a duplicate parent/companion split. Improve the existing course entry and link to it from the stage guide instead. |
| Duke Medical Neuroscience | Defer. [Duke links the course](https://dibs.duke.edu/education/coursera-courses/), but the [course description](https://www.coursera.org/learn/medical-neuroscience) sets first-year medical-school scope and expects cell/molecular biology, physiology, and anatomy. Its depth is useful for a different learner profile; selective textbook chapters fit this pass's bridge better. Full free access was not established from the current enrollment page. |

## Verification boundary

The accepted source pages were opened and compared with current catalog titles and primary URLs. Repository archive checks used the official GitHub API, which reported all three inspected repositories as enabled and not archived on this date. These are dated content and maintenance observations, not guarantees of installation success, exercise correctness, admissions availability, or future support.
