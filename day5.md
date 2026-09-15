# Tag 5

## Was habe ich gelernt?
Ich habe heute ein komplettes Next.js-Projekt lokal eingerichtet: Repo geklont, `npm install`
ausgeführt und den Dev-Server mit `npm run dev` gestartet. Dabei habe ich verstanden, wie
Umgebungsvariablen funktionieren – Variablen mit `NEXT_PUBLIC_`-Präfix sind im Browser
sichtbar, und lokale `.env`-Werte sind komplett getrennt von den Variablen, die man in
Vercel unter Settings → Environment Variables einträgt (die müssen für Production und
Preview separat gepflegt werden).

Außerdem habe ich die Deployment-Pipeline verstanden: Ein Merge in `main` löst automatisch
ein Production-Deployment aus, während jeder offene Pull Request automatisch ein eigenes
Preview-Deployment über die Vercel-GitHub-Integration bekommt. Dazu habe ich ein eigenes
kleines Feature gebaut (Branch `feature-tipp-farbverlauf`): einen Tipp-Effekt für das Motto
mit blinkendem Cursor und einen bunten Glow-Hintergrund, in React/TypeScript mit
CSS-Animationen.

## Welches Problem hatte ich?
Das Vercel-Deployment ist zuerst fehlgeschlagen, weil eine Adress-Variable dort fehlte, die
im Code für einen Impressumspflicht/DSGVO-Check gebraucht wird. Außerdem ist mein Pull
Request zunächst versehentlich an das falsche Repo (einen Fork statt mein eigenes) gegangen.

## Wie habe ich es gelöst?
Ich habe die fehlende Umgebungsvariable in den Vercel-Projekteinstellungen ergänzt, danach
lief der Build durch. Beim Pull Request habe ich das Ziel-Repo korrigiert, sodass er
tatsächlich in meinen eigenen `main`-Branch gemergt wurde – danach hat Vercel automatisch
das neue Production-Deployment ausgelöst und die Änderungen waren live.