# Søk i Fadersrøsten

Søk i innholdsregisteret til tidsskriftet *Fadersrösten*, årgang 1–30 (1960–1989), 545 artikler. Appen bruker samme design og oppsett som [Læstadiansk prekensøk](https://prekensok.github.io/): statisk HTML, ingen server eller byggesteg i nettleseren, og fire språk (norsk, svensk, finsk, engelsk).

Åpne `index.html` i en nettleser.

## Du kan søke på
- bibeltekst: `Luk 15`, `Matt 5:1-12`, `Rom 10,4`. Vers-spenn teller som treff når de overlapper. Bokforkortelser på norsk, svensk, finsk og engelsk virker.
- ord i titler: `nåd`, `Försoning`. Vanlige norske, finske og engelske ord oversettes til svenske ordstammer (`nattverd`, `påske`, `communion`).
- forfatter: `Luther`, `Bunyan`, `S W-n`, `LLL`
- årgang og nummer: `1975`, `1975 nr 2`, `84:2`, `FR 84:2`, `årgang 16`
- nummer i andre prekensamlinger (Læstadius-prekener): `RRS 47`, `SW 17B`, `Saarnat 274`, eller bare `83`

Listene under søkefeltet avgrenser på forfatter og årgang, og kan brukes uten søkeord for å bla.

## Kilder og data
- `../Register/Fadersrosten_register.csv`: innholdsregisteret, transkribert fra fotografier av innholdsfortegnelsene.
- `../../Læstadius/prekensok/data/prekener.js`: Peltomaas *Predikotextregister* (OCR) slått sammen med de andre registrene i prekensøk. FR-kolonnen hans (år:nummer) gir koblingen til registeret.
- `data/fadersrosten.js`: den samlede databasen appen bruker, generert av `tools/bygg_data.py`.
- `tools/koblingsrapport.txt`: alle koblinger der Peltomaas bibeltekst avviker fra den trykte, og prekener uten kobling.

`tools/` og kildene ligger bare lokalt og er ikke med i dette repoet. Kjør på nytt etter endringer i kildene:

```bash
python tools/bygg_data.py
```

Søket dekker innholdsfortegnelsene, ikke artiklenes fulle tekst. Trykte bibelhenvisninger og Peltomaas bibeltekster vises hver for seg og rettes ikke mot hverandre, siden begge kan inneholde feil.
