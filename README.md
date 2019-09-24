# mi-style-lib

Dieses Repository beinhaltet die Style Library der Medieninformatik. Sie wird beispielsweise für die Jekyll Veranstaltungswebsites verwendet.

Styles werden in diesem Repository als SASS/SCSS-Dateien entwickelt und sollen zu einem späteren Zeitpunkt auch als kompillierte Version zum direkten Einbinden bereitgestellt werden.

## Nutzung der Library

Die Einbindung dieser SASS-Library sollte idealerweise über Git Subtree erfolgen. Dafür kann folgender Befehl verwendet werden:

```bash
git subtree add --prefix _sass/lib https://github.com/flobraeun/mi-style-lib.git master --squash
```

Hiermit wird diese Library im Ordner `_sass/lib` des gewünschten Repositories hinzugefügt. Zukünftig lassen sich neue Versionen mittels dieses Befehls abrufen:

```bash
git subtree pull --prefix _sass/lib https://github.com/flobraeun/mi-style-lib.git master --squash
```

Die Hauptdatei und der Einstiegspunkt der Library ist die `mi-styles.scss`-Datei. Über diese werden alle Teile der Library eingebunden. Es können auch gezielt nur einzelne Teile der Library eingebunden werden, die `bulma.sass`-Datei sollte aber in jedem Fall genutzt werden. Ein Beispiel für die Einbindung und Erweiterung dieser Library ist die [`mi-jekyll.scss`-Datei](https://github.com/flobraeun/mi-jekyll-theme/blob/master/_sass/mi-jekyll.scss) des Jekyll Themes für Veranstaltungswebsites der Medieninformatik.
