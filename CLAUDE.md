# CLAUDE.md - Instrucțiuni pentru Claude

## Limba și comunicare
- Limba primară: Doar limba română
- Stil răspuns: Scurt și direct - doar concluzia când execut task-uri
- Nu narezi procesul, doar rezultatul final
- Nu scrie mesaje intermediare între tool call-uri (gen "Acum testez...", "Confirmat...", "Continuu cu...")
- Scrie un singur mesaj, doar la final, după ce ai terminat tot task-ul
- Mesajele ar trebui să fie concise

## Cod și implementare
- Preferă editarea fișierelor existente în loc de a crea fișiere noi
- Nu adauga funcționalități dincolo de ceea ce se cere
- Exclude comentarii în cod
- Testează golden path și edge cases înainte de a raporta finalizarea

## Git și commituri
- Folosesti branch-uri deja create si active in JetBrainsIDE
- Ceri permisiunea de a crea branch-uri noi, PUSH, PR de fiecare data
- Mesajele de commit ar trebui să explice WHY, nu WHAT
- Verifica git status înainte de operații destructive
- Nu folosește --force-push fără confirmarea utilizatorului

## Testing și calitate
- Analizează codul înainte să scrii teste
- Nu modifica implementarea doar pentru ca testele să treacă
- Rulează doar testul failed, nu toate
- Raportează clar testele care eșuează
- Verifică că nu s-au creat regresii în alte feature-uri
- Integreaza testele, nu mock-urile, unde este posibil
- Exclude si fixeaza warnings

## Comunicare cu utilizatorul
- Confirm ințelegerea task-ului înainte de a implementa
- Semnalează blocări imediat
- Oferă recomandări scurte (2-3 propoziții) pentru decizii neaprobate
- Raportează progresul la puncte cheie

### Testare manuala ca un manual QA
- Executi exact ce se cere nu mai mult
- Daca ceva nu intelegi intrebi
- Dupa ce testezi faci o concluzie in care raportezi ce ai testat, bug-uri in care le imparti in categorii dupa severitate, alte observatii
- Bugurile gasite trebuie sa aiba env, description (aici descrii clar, scurt concis si detaliat problema si cum afecteaza) steps to reproduce, expected result, actual status, screenshot
- Cand testezi, nu lasa gunoi in urma: revii exact la starea de dinainte de testare (date create, fisiere temporare, configurari schimbate, etc.)
- Nimic nu ramane modificat, sters sau editat in urma testarii - orice schimbare facuta doar pentru a testa se anuleaza la final
