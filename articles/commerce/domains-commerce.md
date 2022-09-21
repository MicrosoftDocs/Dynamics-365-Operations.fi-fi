---
title: Toimialueet Dynamics 365 Commercessa
description: Tässä artikkelissa kerrotaan, miten toimialueita käsitellään Microsoft Dynamics 365 Commercessa.
author: BrianShook
ms.date: 09/09/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: BrShoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 132aec92d2b3d2765dd6bd261fb4182f8aae679a
ms.sourcegitcommit: dbb997f252377b8884674edd95e66caf8d817816
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/10/2022
ms.locfileid: "9465190"
---
# <a name="domains-in-dynamics-365-commerce"></a>Toimialueet Dynamics 365 Commercessa

[!include [banner](includes/banner.md)]

Tässä artikkelissa kerrotaan, miten toimialueita käsitellään Microsoft Dynamics 365 Commercessa.

Toimialueet ovat verkko-osoitteita, joiden avulla siirrytään Dynamics 365 Commerce -sivustoissa selaimen avulla. Voit ohjata toimialueen hallintaa valitun toimialuenimipalvelimen (DNS) tarjoajan avulla. Toimialueisiin viitataan Dynamics 365 Commerce -sivuston luontiohjelmassa. Niiden avulla määritetään, miten sivustoa käytetään julkaisun jälkeen. Tässä artikkelissa on tietoja toimialueiden käsittelemisestä ja niihin viittaamisesta Commerce-sivuston kehityksen ja käynnistyksen elinkaaren aikana.

> [!NOTE]
> Kaikille Dynamics 365 Commerce -ohjelmassa luoduille ympäristöille valmistellaan `.dynamics365commerce.ms`-toimialue 6.5.2022 alkaen aiemman mallin `.commerce.dynamics.com` tilalle. `.commerce.dynamics.com`-toimialueeseen liittyvät aiemmin luodut ympäristöt jatkavat toimimista.

## <a name="provisioning-and-supported-host-names"></a>Valmistelu ja tuetut isäntänimet

Kun sähköisen kaupankäynnin ympäristöä valmistellaan [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/) -sovelluksessa, sähköisen kaupankäynnin valmistelunäytön **Tuetut isäntänimet** -ruutua käytetään Commerce-ympäristön toimialueiden syöttämiseen. Nämä toimialueet ovat asiakkaille tarkoitettuja DNS-nimiä, joissa sähköisen kaupankäynnin verkkosivustoja isännöidään. Toimialueelle siirtyminen ei tässä vaiheessa aloita liikenteen ohjaamista Dynamics 365 Commercen toimialueelle. Toimialueen liikenne reititetään vain Commercen päätepisteeseen, kun DNS CNAME -tietue päivitetään käyttämään Commercen päätepistettä ja toimialuetta.

> [!NOTE]
> **Tuetut isäntänimet** -ruutuun voidaan syöttää useita toimialueita erottamalla ne puolipisteillä.

Seuraavassa kuvassa on LCS:n sähköisen kaupankäynnin valmistelunäyttö, jossa on **Tuetut isäntänimet** -ruutu korostettuna. 

![LCS:n sähköisen kaupankäynnin valmistelunäyttö ja **Tuetut isäntänimet** -ruutu korostettuna.](./media/Domains_ProvisioningeCommerceScreen_publish.png)

Voit luoda palvelupyynnön lisätoimialueiden lisäämiseksi ympäristöön, jos valmistelu on jo tapahtunut. Jos haluat luoda palvelupyynnön LCS:ssä, siirry ympäristössäsi kohtaan **Tuki \> Tukea vaativat ongelmat** ja valitse **Lähetä tapaus**.

## <a name="commerce-generated-urls"></a>Commercen luomat URL-osoitteet

Sähköisen kaupankäynnin Dynamics 365 Commerce -ympäristön valmistelun yhteydessä Commerce luo URL-osoitteen, joka on ympäristön työosoite. Tähän URL-osoitteeseen viitataan sähköisen kaupankäynnin sivuston linkissä, joka näkyy LCS:ssä ympäristön valmistelun jälkeen. Commercen luoman URL-osoitteen muoto on `https://<e-commerce tenant name>.dynamics365commerce.ms`, jossa sähköisen kaupankäynnin vuokraajan nimi on Commercen ympäristöön LCS:lle syötetty nimi.

Voit käyttää tuotantosivuston isäntänimiä myös eristysympäristössä. Tämä vaihtoehto on ihanteellinen, kun kopioit sivuston eristysympäristöstä tuotantoon.

## <a name="site-setup"></a>Sivuston asetukset

Kun sähköisen kaupankäynnin ympäristö valmistellaan, sivusto on määritettävä Comerce-sivuston luontiohjelmassa ja liitettävä sivusto toimivaan URL-osoitteeseen.

Kun määrität sivuston ensimmäisen kerran sivuston luontiohjelmassa, **Määritä sivusto** -valintaikkuna tulee näkyviin.

Seuraavassa kuvassa näkyy Oletus-nimisen sivuston **Määritä sivusto** -valintaruutu, kun käytät sivustoa ensimmäisen kerran sivuston luontiohjelmassa.

![**Määritä sivusto** -valintaruutu.](./media/Domains_SetupyoursiteScreen.png)

**Valitse toimialue** -ruudussa voit liittää yhden sivustolle LCS:ssä annetuista tuetuista isäntänimistä sivuston luontiohjelmassa.

**Polku**-ruutu voidaan jättää tyhjäksi tai lisäpolun merkkijono voidaan lisätä. Se vaikuttaa käytössä olevaan URL-osoitteeseen. Jos **Polku**-ruutu jätetään tyhjäksi, Commercen luoma perus-URL-osoite liitetään sivuston luontiohjelmassa määritettävään sivustoon. Polkujen on oltava yksilöllisiä kullekin sivusto-/toimialueparille. Valitun sivuston ja toimialueen ympäristön sivustoista vain yksi voi käyttää tyhjää polkua ja vain yksi voidaan liittää yksilöllisen polun merkkijonoon. Mistä tahansa sivuston määrityksen yhteydessä **Polku**-kenttään lisätystä merkkijonosta tulee Commercen luoman perus-URL-osoitteen alipolku. Sen avulla sivustoa käytetään selaimella.

> [!NOTE]
> Polku tunnetaan myös nimellä **match path**, kun kanava lisätään sivuston luontiohjelman **Sivuston asetukset \> Kanavat** -konfigutaation osassa.

Jos sähköisen kaupankäynnin vuokraajassa nimeltä xyz on esimerkiksi sivuston luontiohjelman sivusto nimeltä fabrikam ja määrität sivuston, jolla on tyhjä polku, voit käyttää julkaistua sivuston sisältöä verkkoselaimessa siirtymällä suoraan Commercen luomaan perus-URL-osoitteeseen seuraavasti:

`https://xyz.dynamics365commerce.ms`

Vaihtoehtoisesti voit käyttää julkaistua sivuston sisältöä selaimessa seuraavan URL-osoitteen avulla, jos olet lisännyt fabrikam-polun sivuston asetusten aikana:

`https://xyz.dynamics365commerce.ms/fabrikam`

## <a name="pages-and-urls"></a>Sivut ja URL-osoitteet

Kun sivustosi on määritetty poluksi, kaikki sivuston luontiohjelman sivuihin liittyvät URL-osoitteet perustuvat toimivaan URL-osoitteeseen (Commercen luoma URL-osoite tai Commercen luoma URL-osoite ja polku). Uuden URL-osoitteen luominen sivuston luontiohjelmassa (**URL-osoitteet/ > +Uusi**) valitsemalla sivu **Uusi URL-osoite**-valintaruudun luettelossa ja syöttämällä URL-polku tälle sivulle liittää kyseisen URL-osoitteen valittuun sivuun. Tämän jälkeen URL-polun arvo lisätään sivuston toimivaan URL-osoitteeseen. Osoitteen avulla käytetään sivua. Osoitteen nimi on `./<URL path>` **URL-osoitteet**-sivun URL-osoitteiden luettelossa sivuston luontiohjelmassa.

Seuraavassa kuvassa näkyy **Uusi URL-osoite**-valintaruutu sivuston luontiohjelmassa sekä URL-osoitteen esimerkkipolku korostettuna. 

![**Uusi URL-osoite** -valintaruutu sivuston luontiohjelmassa.](./media/Domains_PageSetup2a.png)

Seuraavassa kuvassa näkyy **URL-osoitteet**-sivu sivuston luontiohjelmassa sekä URL-osoite korostettuna luettelossa.

![Käyttäjän työnkulku -vaihtoehdon suorittaminen käytännön työnkulussa.](./media/Domains_URLsInSiteBuilder2a.png)

## <a name="domains-in-site-builder"></a>Toimialueet sivuston luontiohjelmassa

Tuetut isäntänimien arvot ovat käytettävissä. Ne voidaan liittää toimialueena, kun sivustoa määritetään. Kun tuettua isäntänimen arvoa valitaan toimialueeksi, näkyvissä on valittu toimialue. Siihen viitataan sivuston luontiohjelmassa. Tämä toimialue on vain viite Commerce-ympäristössä. Kyseisen toimialueen suoraa liikennettä ei vielä välitetä Dynamics 365 Commerceen.

Jos olet määrittänyt sivuston luontiohjelmassa kaksi sivustoa, joilla on eri toimialueet, voit liittää **?domain=**-määritteen käytettävään URL-osoitteeseen ja käyttää julkaistun sivuston sisältöä selaimessa.

Ajatellaan, että xyz-niminen ympäristö on valmisteltu ja sivuston luontiohjelmassa on luotu ja liitetty kaksi sivustoa. Toisen toimialue on `www.fabrikam.com` ja toisen `www.constoso.com`. Kukin sivusto on määritetty käyttämällä tyhjää polkua. Näitä kahta sivustoa voidaan tämän jälkeen käyttää selaimessa **?domain=**-määritteen avulla seuraavasti:
- `https://xyz.dynamics365commerce.ms?domain=www.fabrikam.com`
- `https://xyz.dynamics365commerce.ms?domain=www.contoso.com`

Kun toimialueen kyselymerkkijonoa ei anneta ympäristössä, jossa on useita toimialueita, Commerce käyttää ensimmäistä toimialuetta. Jos esimerkiksi polku fabrikam annettiin ensin sivuston asetuksen aikana, URL-osoitetta `https://xyz.dynamics365commerce.ms` voidaan käyttää julkaistun sivuston sisällön käyttämisessä URL-osoitteessa `www.fabrikam.com`.

## <a name="traffic-forwarding-in-production"></a>Liikenteen välittäminen tuotannossa

Voit simuloida useita toimialueita käyttämällä toimialueen kyselymerkkijonon parametreja itse commerce.dynamics.com-päätepisteessä. Kun haluat julkaista tuotannon, sinun on välitettävä liikenne muokattuun toimialueeseen `<e-commerce tenant name>.dynamics365commerce.ms`-päätepisteessä.

`<e-commerce tenant name>.dynamics365commerce.ms`-päätepiste ei tue mukautetun toimialueen SSL (Secure Sockets Layer) -salausta. Määritä siis mukautetut toimialueet käyttämällä Front Door Service -palvelua tai sisällön toimitusverkostoa. 

Jos haluat määrittää mukautettuja toimialueita Front Door Service -palvelun tai sisällön toimitusverkoston (CDN) avulla, käytettävissä on seuraavat kaksi vaihtoehtoa:

- Määritä Front Door Service -palvelu, kuten Azure Front Door Service, joka käsittelee edustaliikennettä, ja muodosta yhteys Commerce-ympäristöön. Tämä parantaa toimialueiden ja varmenteiden hallintaa sekä enemmän yksityiskohtaisia suojauskäytäntöjä.

- Käytä Commercen mukana toimitettua Azure Front Door -esiintymää. Tämä edellyttää Dynamics 365 Commercen ryhmän koordinointitoimintoja toimialueen todentamiseksi ja SSL-varmenteiden hankkimista tuotannon toimialueelle.

> [!NOTE]
> Jos käytössä on ulkoinen CDN tai Front Door Service -palvelu, varmista, että Commerce-ympäristöön saapuvalla pyynnöllä on Commercen antaman isäntänimi, mutta X-Forwarded-Host (XFH) -otsikko \<custom-domain\>. Jos esimerkiksi Commerce-päätepiste on `xyz.dynamics365commerce.ms` ja mukautettu toimialue `www.fabrikam.com`, edelleenlähetetyn pyynnön isännän otsikon on oltava `xyz.dynamics365commerce.ms` ja XFH-otsikon `www.fabrikam.com`.

Lisätietoja CDN-palvelun määrittämisestä suoraan on kohdassa [Sisällön toimitusverkoston (CDN) tuen lisääminen](add-cdn-support.md).

Jos haluat käyttää Commercen mukana toimitettua Azure Front Door -esiintymää, sinun on luotava Commercen käyttöönottoryhmän CDN-määrityksen apua koskeva palvelupyyntö. 

- Anna yrityksen nimi, tuotannon toimialue, ympäristön tunnus ja tuotannon sähköisen kaupankäynnin vuokraajan nimi. 
- Vahvista, onko tämä olemassa oleva toimialue (käytetään parhaillaan aktiivisissa sivustoissa) vai uusi toimialue. 
- Jos kyseessä on uusi toimialue, toimialueen vahvistus ja SSL-varmenne voidaan saada yhdessä vaiheessa. 
- Toimialueelle, joka palvelee olemassa olevaa sivustoa, tarvitaan monivaiheinen prosessi. Sen avulla voidaan määrittää toimialueen vahvistus ja SSL-varmenne. Tämä prosessi sisältää 7 työpäivän palvelutasosopimuksen toimialueen julkaisemiselle. Tämä siksi, että peräkkäisiä vaiheita on useita.

Jos haluat luoda palvelupyynnön LCS:ssä, siirry ympäristössäsi kohtaan **Tuki \> Tukea vaativat ongelmat** ja valitse **Lähetä tapaus**.

> [!NOTE]
> Mukautettuja toimialueita, joissa on SSL, tuetaan vain tuotantoympäristöissä. Muissa kuin tuotantoympäristöissä, kuten eristysympäristössä ja käyttäjän hyväksyntätestauksessa voidaan Commercen luomaa URL-osoitetta julkisen sisällön käyttämisessä selaimessa.

## <a name="ssl-certificate-process"></a>SSL-varmenneprosessi

Kun palvelupyyntö on lähetetty, Commercen ryhmä tekee kanssasi seuraavat vaiheet.

Uudet toimialueet:
- Commercen ryhmä määrittää Azure Front Door -esiintymän (Commercen isännöimä).
- Tämän jälkeen Commercen ryhmä antaa CNAME-tietueen, joka osoittaa mukautettuun toimialueeseen.
- Kun CNAME-tietue on päivitetty, Commercen isännöimä Azure Front Door -esiintymä voi vahvistaa toimialueen omistajan ja saada SSL-varmenteen.

Olemassa olevat / aktiiviset toimialueet:
- Commercemn ryhmä ohjaa sinua lisäämään `afdverify.<custom-domain>` CNAME -tietueen. Sen avulla määritetään toimialueen DNS-tarjoaja.
- Kun olet valmis, Commercen ryhmä lisää toimialueen Azure Front Door -esiintymään ja määrittää lisää DNS TXT -tietueita. Ne lisätään toimialueen DNS:ään.
- Kun TXT-tietueet ovat valmiit, Commercen ryhmä Azure Front Door -päivitykset toimialueelle, joka määrittää SSL-varmenteen.

## <a name="apex-domains"></a>Apex-toimialueet

Commercen toimittama Azure Front Door -esiintymä ei tue Apex-toimialueita (juuritoimialueita, jotka eivät sisällä aliverkkotunnuksia). Apex-toimialueet vaativat IP-osoitteen selvittämisen, ja Commercen Azure Front Door -esiintymä on olemassa vain virtuaalisten päätepisteiden yhteydessä. Jos haluat käyttää Apex-toimialuetta, käytettävissä ovat seuraavat vaihtoehdot:

- **Vaihtoehto 1**: Käytä DNS-toimittajaa ja ohjaa Apex-toimialue uudelleen www-toimialueelle. Esimerkiksi fabrikam.com ohjaa uudelleen osoitteeseen `www.fabrikam.com`, jossa `www.fabrikam.com` on CNAME-tietue, joka viittaa Commercen isännöimään Azure Front Door -esiintymään.

- **Vaihtoehto 2** - Jos DNS-toimittaja tukee ALIAS-tietueita, voit osoittaa apex-toimialuetta Azure Front Door -päätepisteeseen. Näin varmistetaan, että päätepisteen IP-muutos otetaan huomioon. Isännöi Azure Front Door -esiintymää itse.
  
- **Vaihtoehto 3** - Jos DNS-toimittaja ei tue ALIAS-tietueita, muuta DNS-toimittajaksi Azure DNS ja isännöi sekä Azure DNS- että Azure Front Door -esiintymää itse.

> [!NOTE]
> Jos käytät Azure Front Door -palvelua, sinun on määritettävä myös Azure DNS -palvelu samassa tilauksessa. Azure DNS:n isännöimä Apex-toimialue voi osoittaa Azure Front Door -palveluun alias-tietueena. Tämä on ainoa ratkaisu, koska Apex-toimialueiden on aina osoitettava IP-osoitteeseen.
  
Jos sinulla on Apex-toimialueiden toimintaan liittyviä kysymyksiä, ole yhteydessä [Microsoft-tukeen](https://support.microsoft.com/).

  ## <a name="additional-resources"></a>Lisäresurssit

  [Uuden sähköisen kaupankäynnin vuokraajan käyttöönotto](deploy-ecommerce-site.md)

  [Määritä verkkokauppakanava](./channel-setup-online.md)

  [Sähköisen kaupankäynnin sivuston luominen](create-ecommerce-site.md)

  [Dynamics 365 Commerce -sivuston liittäminen online-kanavaan](associate-site-online-store.md)

  [Robots.txt-tiedostojen hallinta](manage-robots-txt-files.md)

  [URL-uudelleenohjausten joukkolataus palveluun](upload-bulk-redirects.md)

  [B2C-vuokraajan määrittäminen Commercessa](set-up-B2C-tenant.md)

  [Mukautettujen sivujen määrittäminen käyttäjän kirjautumisia varten](custom-pages-user-logins.md)

  [Useiden B2C-vuokraajien määrittäminen Commerce-ympäristössä](configure-multi-B2C-tenants.md)

  [Sisältöverkon (CDN) tuen lisääminen](add-cdn-support.md)

  [Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
