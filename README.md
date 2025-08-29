# Latex-THM

Dieses LaTeX-Template kann für Praxisphasenberichte und Projektstudiumsberichte verwendet werden. 

Hinweise zur Verwendung des Templates und zur Einbindung von / Arbeit mit Literatur sind im [Leitfaden](./Leitfaden.MD) zu finden.

In das Template wurden die neuen Vorgaben der Richtlinie zum wissenschaftlichen Arbeiten, Stand Februar 2025 eingepflegt. 

Der Rest dieses README folgt dem Original, aus dem dieses Repo geforkt wurde. 

## Getting Started

### LaTex Version

Clone this repo and modify the [document.tex](./document.tex) file according to your needs. See [here](./document.pdf) for a preview.

## Custom commands

### DocumentType

Set the document type with:

```latex
\documentType{Praxisphasenbericht}{SS 2020}
```

As second argument a short description (e.g. semester) can be supplied. Use `{}` for empty description.

### Author

The standard author command of LaTex is overriden

```latex
\author{Your Name}{Your zip code}{Your place}{Your address}{Your matnr}
```

Supply additional information like shown above. Use `{}` for empty description

### Title

No custom command but you'll need it to set the title of your report.

```latex
\title{Your title}
```

### Company supervisor

Set your company supervisor with:

```latex
\companysupervisor{Name}
```

### University supervisor

Set your unversity supervisor with:

```latex
\unisupervisor{Name}
```

### Company

Set company information.

```latex
\company{Company name}{company zip code}{company place}{company address}{Bilder/logo.png}
```

### Maketitle

Use the standard `\maketitle` command to generate your title page. All your information will be added automatically.

### Makeinsurance

Use `\makeinsurance` for generating a insurance section. All your information will be added automatically.

### Lock mark

Adds a generic lock mark to your document.

```latex
\lockMark
```

### Common acronyms

Adds a statement about the usage of common known acronyms.

```latex
\commonAcronyms
```
