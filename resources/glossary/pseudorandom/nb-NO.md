---
term: PSEUDO-RANDOM

---
Dette adjektivet brukes for å beskrive en tallrekke som, selv om den er et resultat av en deterministisk prosess, har egenskaper som ligger nær egenskapene til en ideell, virkelig tilfeldig rekkefølge. Begrepet ideell tilfeldighet innebærer et totalt fravær av forutsigbarhet og korrelasjon mellom suksessive elementer. Et pseudotilfeldig tall genereres av en deterministisk algoritme og er derfor i teorien helt forutsigbart hvis man kjenner generatorens opprinnelige tilstand.

En pseudotilfeldige tallgenerator (PRNG) er en algoritme som brukes til å produsere slike tall. Den tar vanligvis utgangspunkt i en startverdi, eller "seed", og bruker deretter en rekke matematiske transformasjoner for å produsere tallsekvensen. På grunn av denne bestembarheten er det viktig for kryptografisk sikkerhet at startverdien forblir hemmelig. Pseudotilfeldige sekvenser er mye brukt på ulike områder, inkludert kryptografi, ettersom de har en tilsynelatende tilfeldig oppførsel som er tilstrekkelig for mange anvendelser. Evalueringen av kvaliteten til en PRNG er basert på i hvilken grad utdataene nærmer seg ekte tilfeldighet når det gjelder fordeling, korrelasjoner og andre statistiske egenskaper. I forbindelse med Bitcoin brukes pseudotilfeldige tall til å produsere private nøkler, eller til å generere et seed for deterministiske og hierarkiske lommebøker.