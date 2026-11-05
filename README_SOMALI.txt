ICE BOT - WEBSITE STARTER (DEMO)

MUHIIM:
- Tani waa bog login iyo dashboard DEMO ah.
- OTCharts API kuma xirna weli.
- Ma soo saarayo CALL/PUT dhab ah, mana aha talo maalgashi.
- Ha gelin password-kaaga Quotex.

DEPLOY:
1. Ka fur ZIP-kan Android-ka oo Extract samee.
2. GitHub ka samee repository cusub oo la yiraahdo ice-bot.
3. Soo geli dhammaan faylasha iyo folder-ka templates iyo static (ha soo gelin ZIP keliya).
4. Render.com ka samee account, dooro New > Web Service, kadib ku xiro GitHub repo-ga ice-bot.
5. Build command: pip install -r requirements.txt
6. Start command: gunicorn app:app
7. Environment Variables ku dar:
   SECRET_KEY = xarfo dhaadheer oo qarsoodi ah
   ADMIN_USERNAME = magaca aad rabto
   ADMIN_PASSWORD_HASH = hash-ka password-ka (eeg tilmaanta hoose)
8. Deploy kadib Render wuxuu ku siinayaa URL.

PASSWORD HASH:
Si aad hash u samaysato, kombiyuutar ama Python terminal ku orod:
python -c "from werkzeug.security import generate_password_hash; print(generate_password_hash('PASSWORD_KAAGA'))"
Ku beddel PASSWORD_KAAGA password aad adigu dooratay, kadib natiijada geli ADMIN_PASSWORD_HASH.
Android keliya haddii ay kugu adkaato, marka hore ii sheeg meesha aad marayso; ha soo dirin password-kaaga.

ADMIN LOGIN:
Username-ka iyo password-ka aad Environment Variables ku dejisay ayaa ah Admin login-ka.
Account-yo kale oo users ah weli laguma darin starter-kan.
