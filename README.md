# IN1030 Oblig 5: Modellering av krav

Installer og start Podman:

```console
$ brew install podman
$ podman machine init
$ podman machine start
```

Klon repoet og kompiler markdownfilen til en PDF-fil:

```console
$ cd ~/repos
$ git clone https://github.com/fredfoss/in1030oblig5.git
$ cd in1030oblig5
$ make
```

Du har nå PDF-filen `~/repos/in1030oblig5/oblig5.pdf`.

For å kunne gjøre og sende inn endringer i markdownfilen, må du først opprette en GitHub konto, og legge inn en SSH-nøkkel.

* [Creating an account on GitHub](https://docs.github.com/en/get-started/start-your-journey/creating-an-account-on-github)
* [Generating a new SSH key and adding it to the ssh-agent](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
* [Adding a new SSH key to your GitHub account](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)

Så må du klone repoet på denne måten istedet:

```console
$ cd ~/repos
$ git clone git@github.com:fredfoss/in1030oblig5.git
$ cd in1030oblig5
```

Etter å ha gjort en endring i `oblig5.md` og kompilert til PDF med `make`, push endringene til remote origin (GitHub):

```console
$ git add .
$ git commit -m "kort beskrivelse"
$ git push
```

For å laste ned nyeste endringer (husk å `git add` og `git commit` endringene dine først):

```console
$ git pull
```

Kan også sikkert endre filene direkte på github.com.
