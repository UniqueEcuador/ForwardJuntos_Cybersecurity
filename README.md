# ForwardJuntos_Cybersecurity
ForwardJuntos · Phishing Forensics
Tweelaags e-mailanalyse — lokaal + AI-diepteanalyse
Onderdeel van het ForwardJuntos Cybersecurity-pakket · Heerlen, NL


Wat doet dit?
Een forensische phishing-detector die twee lagen combineert:

Laag 1 · Lokale engine (direct, niets verlaat je browser)

URL-forensics: homoglyph-aanvallen, punycode-domeinen, typosquatting (~30 NL-merken), merknaam-in-subdomein-misbruik, @-truc, IP-hosts, verdachte TLD's, URL-verkorters
Header-forensics: From ≠ Reply-To, vervalste weergavenamen, SPF/DKIM/DMARC-resultaten
Psycholinguïstiek: urgentie, angst, hebzucht, autoriteit, geheimhoudingsverzoeken, CEO-fraude-patronen (NL + EN) — met benoemde cognitieve biases
HTML-forensics: tracking-pixels, linktekst ≠ werkelijke bestemming, verborgen tekst

Laag 2 · AI-diepteanalyse (optioneel, eigen API-sleutel vereist)
Elite-analist-prompt: psychologische manipulatietechnieken, linguïstische anomalieën, infrastructuurkenmerken en contextuele incongruenties — met JSON-output (risicoscore, classificatie, rode vlaggen, handelingsadvies).


Gebruik
Plaats index.html in een map of serveer hem via je lokale server
Open in je browser
Plak de e-mailtekst (+ optioneel: ruwe headers, losse URL)
Klik Volledige forensische analyse

Voor de AI-laag: open ⚙ instellingen en vul je Anthropic API-sleutel in.
De sleutel blijft lokaal in je browser — staat nooit in dit bestand.


Classificaties
Score
Classificatie
Betekenis
0–29
✅ VEILIG
Geen alarmsignalen gevonden
30–54
⚠️ VERDACHT
Meerdere waarschuwingssignalen — verifieer via officieel kanaal
55–99
🚨 PHISHING
Sterke aanwijzingen voor phishing — niet op reageren
55–99 + gericht
🎯 SPEAR_PHISHING
Gerichte aanval met persoonlijke elementen — extra gevaarlijk



De gouden regel
Een score van 0 is geen garantie.
Bij twijfel: verifieer altijd via een ander kanaal.
Bel de organisatie zelf — gebruik het nummer van hun officiële website, niet het nummer in de mail.


Privacy
Laag 1 draait volledig lokaal. Geen data verlaat je browser.
Laag 2 stuurt de geplakte e-mailtekst naar de Anthropic API. Gebruik dit niet voor e-mails met gevoelige persoonsgegevens van anderen.
De API-sleutel wordt alleen opgeslagen in localStorage van je browser.


Bestanden
Cybersecurity/

├── index.html      # de volledige tool (één bestand, geen dependencies)

└── README.md       # dit bestand


Toekomstige uitbreidingen (backlog)
Attachment-analyse (bestandsnaam-patronen, dubbelextensies)
QR-code URL-extractie
Exporteer rapport als PDF
Offline-modus: marked.js lokaal bundelen



ForwardJuntos · van overleven naar leven · forwardjuntos.nl
