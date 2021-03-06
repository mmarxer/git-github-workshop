<!-- $theme: default -->

<!-- Presentation made with [Marp](https://yhatt.github.io/marp/) -->
# Git & Github Workshop
# ![](https://s3-us-west-2.amazonaws.com/airskul/2016-06-02%2015:26:20-998-1464881180--997086473.jpg)

###### open\HSR ( [@openhsr](https://github.com/openhsr) )
---

# GitHub bietet...

* **Git Hosting**
* **Pull Requests** - mehr dazu später!
* **Issue Tracker**
* Hosting statischer Webseiten
* Integration in Drittdienste
  * Bsp. Continous integration mit Travis-CI usw.
* Vieles, vieles mehr …

---

# Git Remotes

<div style="text-align: center">
  
![](../notes/images/github-setup.svg)

</div>

---

# Exkurs: Protokolle

## HTTP(S): `https://github.com/openhsr/verein.git`

## SSH: `git@github.com:openhsr/verein.git`

## (Lokales Dateisystem)

---

# Neues Remote einrichten und verwenden

Neues "Remote" erstellen:
```bash
git remote add origin git@github.com:user/repo.git
```

Commits an Remote `origin` schicken:
```bash
git push origin master
```

---

# Bestehendes online-Repo herunterladen

`git help clone`:
```bash
git clone <repository> [<directory>]
```

also z.B:
```bash
git clone https://github.com/openhsr/verein.git
```

---

# Änderungen aus online-Repo herunterladen

```bash
git fetch
# Remote-Änderungen sind jetzt nur in origin/master

git merge origin/master
# Jetzt auch im aktuellen branch (master)
```

Alles in einem:

```bash
git fetch --rebase
# oder noch einfacher:
git pull
```

---

# Repetition an der Grafik


<div style="text-align: center">
  
![](../notes/images/github-setup.svg)

</div>

---

# 🍽️ GitHub Flow

Prozess, wie zusammengarbeitet wird auf GitHub.

1. *Fork* (=Kopie) vom Originalprojekt auf GitHub anlegen
2. Änderungen auf *Fork* umsetzen
   1. `git clone <fork>`
   2. 📝; `git add`; `git commit`
   3. `git push` (zum Fork)
4. Erstellen von *Pull Request* mit Änderungen
   <small>vom Fork zum Originalprojekt</small>
6. Originalprojekt übernimmt / *Merged* den *Pull Request*
   <small>oder erbittet Änderungen /  lehnt diesen ab</small>

---

# ...und nochmal diese Grafik


<div style="text-align: center">
  
![](../notes/images/github-setup-pull.svg)

</div>

---

# 📨 Gästebuch

### ➡️ Fork https://github.com/openhsr/git-github-workshop/
### ➡️ `git clone`; `git checkout guestbook`
### ➡️ `git add  VornameName.md`; `git commit`
### ➡️ `git push`
### ➡️ Open Pull Request
