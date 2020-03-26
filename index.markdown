---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

![Logo_WhiteBG.png](/logo/Logo_WhiteBG.png)

MitigationHubs bringt das Projekt #flattenthecurve in Eure Wohnzimmer! Welche Region dämmt außergewöhnlich gut die Corona-Pandemie ein? Und wieso? Der Kampf gegen das Virus ist eine wissenschaftlichen Aufgabe, welche die Beteilung der Bürger:innen benötigt. Lasst uns kooperien, lasst uns positive Stories über Corona erzählen und daraus lernen!

*MitigationHubs ist ein Beitrag zum [#WirVsVirusHack](https://twitter.com/WirvsVirusHack)*

# Mehr über das Projekt

[Pitch Video auf YouTube](https://www.youtube.com/watch?v=c1ocxDVbZk0&feature=youtu.be)          [Projekt auf Devpost](https://devpost.com/software/landkreis-basierte-datenanalyse-der-fallzahlen-njehgr)          [Projektbeschreibung](/project.markdown)

## Ablauf

1. Aufruf zur Unterstützung von Wissenschaftler:innen durch Meldung von Maßnahmen und das Sammeln von Fragen durch Bürger:innen
2. Analyse der RKI Daten sowie anonymen Daten zur lokalen Eindämmung und Identifikation von positiven Abweichlern durch das Wissenschaftsteam (siehe Fallbeispiele unten)
3. Rückmeldung der Ergebnisse an die partizipierenden Bürger:innen und die allgemeine Öffentlichkeit

## Mach mit und melde die Maßnahmen gegen die Ausbreitung des Coronavirus vor deiner Haustür!

*Zum Mitmachen bitte auf den Button klicken*

<div style="text-align:left">
	<a href="https://forms.gle/3Jd2hRYbJGRBZ42d6?hl=de">
		<img src="/logo/MachMitButton.png" alt="Mach mit!" title="MachMitButton.png" width="300" />
	</a>
</div>
<br/>

# Fallbeispiele
In den 48 Stunden des #WirVsVirusHack haben wir mit unseren Methoden drei Fallbeispiele betrachtet, die mögliche Analysen illustrieren. Entscheidend für die Identifikation von MitigationHubs, sind neben den aktuellen Fallzahlen vor allem Kenntnisse über lokale Maßnahmen, die eine Eindämmung der weiteren Verbreitung des Covid19-Virus zum Ziel haben. Hierfür brauchen wir die Beteiligung der Bürger:innen.

## Forschungsfragen
- Welche Landkreise und Regionen schaffen es im Vergleich besonders gut die Ausbreitung des Covid19-Virus zu verlangsamen?
- Was kann die Bundesrepublik von diesen positiven Abweichlern lernen? 
- Auf welche Maßnahmen sollte ich als Bürger:in besonderen Wert legen?
  
## Fallbeispiel 1: Vergleich der Fallzahlenentwicklung im und um den Landkreis Heinsberg
![case_study_landkreise.png](/plots/case_study_landkreise.png)
*Fallbeispiel 1: Vergleich der Fallzahlenentwicklung im und um den Landkreis Heinsberg*

Landkreise in Deutschland unterscheiden sich anhand vieler Merkmale:
- ihre generelle Struktur, also zum Beispiel die Bevölkerungsdichte, handelt es sich um eine Großstadt oder ländliche Region, Einkommen, und Altersgruppenverteilung,
- wann die ersten positiven Fälle gefunden wurden,
- und wann welche Maßnahmen zur Eindämmung des Virus getroffen wurden.

Hier vergleichen wir vier Landkreise, in direkter oder nahezu direkter Nachbarschaft zueinander: 
- den Landkreis Heinsberg, in dem sehr früh Fälle aufgetreten sind, und der dementsprechend früh Maßnahmen zur Eindämmung getroffen hat,
- die StadtRegion Aachen,
- den Landkreis Düren,
- und den Stadtkreis Köln.

Die Daten, zu denen gewisse Maßnahmen eingeführt wurden, sind hierbei den Webseiten der Landkreise entnommen. Bis auf die Schulschließungen im Landkreis Heinsberg stimmen diese mit der Einführung der Maßnahmen auf Landesebene überein. Für die Veranstaltungsverbote und Ladenschließungen ist jeweils das Datum, zu dem der Beschluss veröffentlicht wurde, aufgeführt.

Die Fallzahlen sind logarithmisch aufgetragen, um potentielles exponentielles Wachstum, das bei ungebremster Ausbreitung des Virus zu erwarten ist, besser sichtbar zu machen. Schon mit bloßem Auge lassen sich Änderungen im Anstieg erkennen. Um diese belastbar statistisch zu untersuchen und zum Beispiel die Wirksamkeit von Maßnahmen zu belegen oder Prediktoren zu finden, die einen Landkreis besonders widerstandsfähig machen, decken die Daten noch einen zu geringen Zeitraum ab. Um eine solche Analyse auf ganz Deutschland auszuweiten, müssten v.a. auch die Daten zur Einführung verschiedener Maßnahmen gesammelt werden. Mit dem anwachsenden Datenvolumen in den nächsten Wochen, hätte eine Analyse (z.B. eine breakpoint analysis), aber das Potenzial regionale Trends sichtbar zu machen und besonders wirksame Maßnahmen hervorzuheben. 


## Fallbeispiel 2: Relation von verschiedenen Einflussfaktoren auf die Wachstumsrate von Covid19-Fällen

Um zu schauen wie sich individuelle Maßnahmen von Regionen auf die Wachstumsraten der Covid19-Fälle auswirken, versuchen wir die erwarteten Wachstumsraten ohne individuelle Maßnahmen möglichst genau vorherzusagen. Um die sozio-ökonomische Vielfalt und ihre Auswirkungen auf die Wachstumsraten zu berücksichtigen, testen wir den Einfluss von verschiedenen Einflussfaktoren auf die Wachstumsraten und die absoluten Fallzahlen.

![arrow_plot_lasso.png](/plots/arrow_plot_lasso.png)
*Fallbeispiel 2: Positive (rot) und negative Korrelationen (Blau) zwischen der Wachstumsrate von Covid19-Fällen und verschiedenen Prediktoren*

Mittels einer sogenannten Lasso Regression, ermitteln wir aus verschiedenen potentiellen Einflussfaktoren diejenigen, die die Fallzahlen am besten erklären. Zum Beispiel führt auf Landkreisebene ein hoher Anteil an jungen Menschen und ein hohes Durchschnittseinkommen aktuell zu höheren Gesamtfallzahlen (pro 100.000 Einwohner), während ein hoher Anteil an alten Menschen und ein hoher Bewegungsradius pro Tag aktuell mit niedrigeren Gesamtfallzahlen einhergeht.

![arrow_plot_lasso.png](/plots/scatter_plot_predictors.png)
*Fallbeispiel 2: Eine Regressionsmethode prüft die Signifikanz von Einflüssen auf die Fallzahlen, hier durch die Demographie & das Einkommen*

Der statistische Zusammenhang zwischen einzelnen Faktoren und den Fallzahlen kann über Scatterplots und lineare Regressionen (siehe Abbildung oben) analysiert werden. In der linken Abbildung sieht man wie auf Bundeslandebene ein höherer Anteil an alten Menschen mit niedrigeren Fallzahlen zusammenhängt. Allerdings hat der Altenquotient wenig Einfluss auf die aktuellen Wachstumsraten, sodass sich dieser Zusammenhang in naher Zukunft ändern kann und regelmäßig mit neuen Zahlen überprüft werden muss. Auf Landkreisebene findet sich aktuell ein schwacher positiver Zusammenhang zwischen Fallzahlen und Einkommen.

Wichtig ist, dass diese Faktoren nicht unbedingt mit Kausalität einhergehen. Aber sie können genutzt werden, um Hypothesen über die Ausbreitung des Virus zu unterstützen und wiederlegen. Stetig aktualisierte Daten und eine Überprüfung weiterer Einflussfaktoren können unsere vorläufigen Ergebnisse verbessern.

# Referenzen

RKI Dashboard zu Fallzahlen auf Bundesland- und Landkreisebene: [https://experience.arcgis.com/experience/478220a4c454480e823b17327b2bf1d4/page/page_1/](https://experience.arcgis.com/experience/478220a4c454480e823b17327b2bf1d4/page/page_1/)

RKI Datensätze auf Landkreiseebene: [https://npgeo-corona-npgeo-de.hub.arcgis.com/search?groupIds=b28109b18022405bb965c602b13e1bbc](https://npgeo-corona-npgeo-de.hub.arcgis.com/search?groupIds=b28109b18022405bb965c602b13e1bbc)

Mobilität in Deutschland: [https://www.mobilitaet-in-tabellen.de/mit/](https://www.mobilitaet-in-tabellen.de/mit/)

Raumtypologie Deutschland: [https://www.bmvi.de/SharedDocs/DE/Artikel/G/regionalstatistische-raumtypologie.html](https://www.bmvi.de/SharedDocs/DE/Artikel/G/regionalstatistische-raumtypologie.html)

Demographische und Soziographische Daten: [https://www.algoly.com/](https://www.algoly.com/)

Krankenhäuser und Anzahl an Betten: [https://npgeo-corona-npgeo-de.hub.arcgis.com/datasets/348b643c8b234cdc8b1b345210975b87_0?geometry=-21.114%2C46.261%2C42.168%2C55.880m](https://npgeo-corona-npgeo-de.hub.arcgis.com/datasets/348b643c8b234cdc8b1b345210975b87_0?geometry=-21.114%2C46.261%2C42.168%2C55.880m)
