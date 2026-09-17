I added a convention to CLAUDE.md: hungarian notation, because I like it

I have cut CLAUDE.md: dropped npm start (redundant with npm run dev) and the separate tests/ architecture bullet (already

&#x20; 			covered by the server.js line), and tightened the remaining wording.



I have added this rules to settings.json:



&#x20;   "allow" permission: Bash(npm test:\*)

&#x20;   "ask" permission: Bash(git push:\*)"

&#x20;   "deny": Read(./.env), Bash(git push --force:\*)



&#x09;itt a deny permission nélkül a CLAUDE érzékeny adatokat olashatna a projekt gyökérből ami később máshova is bekerülhetne

&#x20; 

