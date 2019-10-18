---
title: Kulujenhallinnan mobiilityötila
description: Tässä ohjeaiheessa on tietoja kulujen hallinnan mobiilityötilasta. Työtilan avulla käyttäjät voivat siepata ja ladata kuitteja, jotka voi liittää myöhemmin kuluraportteihin. Käyttäjät voivat myös luoda nopeasti kulurivin liitteenä olevan kuitin avulla sekä luoda ja hallita omia kuluraporttejaan.
author: KimANelson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 8f20202f9e1cf0a8c5d6f48815d456ce7c170259
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187610"
---
# <a name="expense-management-mobile-workspace"></a>Kulujen hallinnan mobiilityötila

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on tietoja **Kulujen hallinta** -mobiilityötilasta. Työtilan avulla käyttäjät voivat siepata ja ladata kuitteja, jotka voi liittää myöhemmin kuluraportteihin. Käyttäjät voivat myös luoda nopeasti kulurivin liitteenä olevan kuitin avulla sekä luoda ja hallita omia kuluraporttejaan. Hyväksyjät voivat myös tarkastella heille määritettyjä kuluraportteja **Kulujen hallinta** -mobiilityötilassa sekä joko hyväksyä tai hylätä nämä kuluraportit.


Tätä mobiilityötilaa on tarkoitettu käytettäväksi Dynamics 365 Unified Ops -sovelluksella.


## <a name="overview"></a>Yleiskuvaus

Moni organisaatio edellyttää, että työntekijän hyvitettäväksi lähetettäviin matka- tai yritystoimintaan liittyvään kuluraporttiin liitetään kuitti. **Kulujenhallinnan** mobiilityötilan avulla käyttäjät voivat nopeasti luoda uusia kulurivejä valitsemassaan mobiililaitteessa liittämällä kuitista valokuvakopion. Käyttäjät voivat myös ottaa kuvan kuitista ja liittää sen kuluraporttiin myöhemmin. Työntekijät voivat myös luoda ja hallita kuluraporttejaan sekä lähettää ne sitten hyväksyttäviksi ja hyvitettäviksi mobiililaitteestaan.


Käyttäjät voivat tehdä **Kulujen hallinta** -mobiilityötilassa seuraavat tehtävät:

- ottaa kuvan kuitista ja ladata sen Dynamics 365 Financeiin. Voit sitten liittää kuvan kuluraporttiin myöhemmin.
- Ladata tiedoston siepattuna kuittina. Voit sitten liittää tiedostoon kuluraporttiin myöhemmin.
- Luoda uuden kulurivin liitetystä kuitista. Voit sitten lisätä rivinimikkeen kuluraporttiin myöhemmin, ja lähettää sen hyväksyntää ja hyvitystä varten.

Voit käyttää myös seuraavia toimintoja:

- Luo uusi kuluraportti.
- Liitä luottokorttitapahtumat ja muut aiemmin luodut kulut kuluraporttiin.
- Luo uudet kulut kuluraporttiin.
- Liitä kuitti kuluraportin kuluun, joko ottamalla kuva kuitista tai lataamalla tiedosto tarkistettuna kuittina.
- Lisää yrityksen kulukäytännön mukaisesti vierasluettelo kuluun.
- Erittele kulut yrityksen kulukäytäntöjen mukaisesti.
- Lähetä kuluraportti hyväksyttäväksi ja hyvitettäväksi.
- Hyväksy tai hylkää kuluraportit, joiden hyväksyjäksi sinut on määritetty.

## <a name="prerequisites"></a>Edellytykset
Edellytykset vaihtelevat sen mukaan, mikä versio on otettu käyttöön organisaatiossa.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Edellytykset, jos käytössä on Dynamics 365 Finance 
Jos Finance on otettu käyttöön organisaatiossa, järjestelmänvalvojan on julkaistava **Kulujenhallinta**-mobiilityötila. Ohjeet ovat ohjeaiheessa [Mobiilityötilan julkaiseminen](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Edellytykset, jos käytössä on versio 1611 ja Platform update 3 tai uudempi
Jos organisaatiossa on otettu käyttöön versio 1611 ja Platform update 3 tai uudempi, järjestelmänvalvojan on toteutettava seuraavat edellytykset. 

<table>
<thead>
<tr class="header">
<th>Edellytys</th>
<th>Rooli</th>
<th>kuvaus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ota KB 4019015 käyttöön.</td>
<td>Järjestelmänvalvoja</td>
<td>KB 4019015 on X++-päivitys tai metatietojen korjaus, joka sisältää <strong>Kulujen hallinta</strong> -mobiilityötilan. Järjestelmänvalvojan on toimittava seuraavasti asentaakseen KB 4019015 -päivityksen.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Metatietojen hotfix-korjauksen lataaminen Microsoft Dynamics Lifecycle Servicesistä (LCS)</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Asenna metatietojen korjaustiedosto</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Luo käyttöön otettava paketti</a>, joka sisältää <strong>ApplicationSuite</strong>- ja <strong>ExpenseMobile</strong>-mallit ja lataa sitten käyttöön otettava paketti LCS:ään.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Ota käyttöönotettava paketti käyttöön</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Julkaise <strong>Kulujen hallinta</strong> -mobiilityötila.</td>
<td>Järjestelmänvalvoja</td>
<td>Lisätietoja on ohjeaiheessa <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Mobiilityötilan julkaiseminen</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Lataa ja asenna Dynamics 365 for Operations mobile -sovellus.
Lataa ja asenna Dynamics 365 Unified Ops -mobiilisovellus:

- [Android-puhelimet](https://go.microsoft.com/fwlink/?linkid=850662)
- [IPhone-puhelimet](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Kirjautuminen mobiilisovellukseen
1. Käynnistä sovellus mobiililaitteessa.
2. Anna Dynamics 365 -URL-osoitteesi.
4. Käyttäjänimi ja salasana kysytään, kun kirjaudut sovellukseen ensimmäisen kerran. Kirjota tunnistetiedot.
5. Kun olet kirjautunut sisään, yrityksen käytettävissä olevat työtilat ovat näkyvissä. Huomaa, että jos järjestelmänvalvoja julkaisee uuden työtilan myöhemmin, mobiilityötilojen luettelo on päivitettävä.


[![Nouda päivitettäväksi](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Kuittien sieppaaminen kulujenhallinnan mobiilityötilassa

1. Avaa **Kulujen hallinta** -työtila mobiililaitteessa.
2. Valitse **Sieppaa kuitti**.
3. Valitse **Ota kuva** tai **Valitse kuva**.
4. Noudata seuraavia ohjeita:

    - Jos valitsit **Ota kuva** -vaihtoehdon, toimi seuraavasti:

        1. Sinut siirretään mobiililaitteesi kameraan, jotta voit ottaa kuitista kuvan. Kun olet ottanut kuvan, hyväksy se valitsemalla **OK**.
        2. Valinnainen: Anna kuvalle nimi ja syötä muistiinpanoja.

    - Jos valitsit **Valitse kuva**, toimi seuraavasti:

        1. Valitse kuva luettelosta.
        2. Valinnainen: Anna kuvalle nimi ja syötä muistiinpanoja.

5. Valitse **Valmis**.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Kulujen kirjaaminen nopeasti kulujen hallinnan mobiilityötilassa
1. Avaa **Kulujen hallinta** -työtila mobiililaitteessa.
2. Valitse **Kulun pikasyöttö**.
3. Valitse kulun luokka. Näet luettelon kululuokista, jotka on ladattu sovellukseesi offline-käyttöä varten. Oletusarvon mukaan ladataan 50 nimikettä, mutta sovelluskehittäjä voi muuttaa tätä määrää. Sovelluskehittäjille on lisätietoja ohjeaiheessa [Mobiiliympäristö](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md). Jos luokka ei ole luettelossa, tee verkkohaku valitsemalla **Hae**. Etsi kululuokan tai -tyypin perusteella.
4. Anna kulun tapahtumapäivämäärä.
5. Valinnainen: anna kulun myyjä.
6. Syötä kulun summa.
7. Valitse kulun valuutta. Näet luettelon valuuttakoodeista, jotka on ladattu sovellukseesi offline-käyttöä varten. Oletusarvoisesti ladataan 400 valuuttaa, mutta sovelluskehittäjä voi muuttaa tätä määrää. Sovelluskehittäjille on lisätietoja ohjeaiheessa [Mobiiliympäristö](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md). Jos valuutta ei ole luettelossa, tee verkkohaku valitsemalla **Hae**. Etsi valuutan tai nimen mukaan.
8. Valitse **Ota kuva** tai **Valitse kuva**.
9. Noudata seuraavia ohjeita:

    - Jos valitsit **Ota kuva**, sinut siirretään mobiililaitteesi kameraan, jotta voit ottaa kuitista kuvan. Kun olet ottanut kuvan, hyväksy se valitsemalla **OK**.
    - Jos valitsit **Valitse kuva**, valitse kuva luettelosta.

10. Valitse **Valmis**.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Kuluraportin hyväksyminen kulujen hallinnan mobiilityötilassa (jos käytössä on heinäkuun 2017 päivitys)
1. Avaa **Kulujen hallinta** -työtila mobiililaitteessa.
2. **Kulujen hyväksynnät** näyttää, kuinka monta kuluraporttia on määritetty sinulle hyväksyttäväksi. Luku päivitetään noin 30 minuutin välein. Valitse **Kulujen hyväksynnät**.

    Luettelo sinulle hyväksyttäväksi määritetyistä kuluraporteista avautuu.
    
3. Voit tarkastella kulujen erittelyä valitsemalla kuluraportin.
4. Voit tarkastella erittelyä valitsemalla kulun. Näytettäviä kulutietoja ovat esimerkiksi mahdolliset kuitit, vieraat ja erittelyt.
5. Valitse **Kuluraportti**-sivulla, hyväksytkö vai hylkäätkö kuluraportin.
6. Anna mahdolliset hyväksymistoimintoon liittyvät kommentit.
7. Valitse **Valmis**.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Uuden kuluraportin luominen ja sen lähettäminen hyväksyminen kulujen hallinnan mobiilityötilassa (jos käytössä on heinäkuun 2017 päivitys)
1. Avaa **Kulujen hallinta** -työtila mobiililaitteessa.
2. Valitse **Kulumerkintä**.
3. Valitse joko **Uusi raportti** tai valitse luettelosta aikaisemmin luotu kuluraportti.
4. Jos kyse on uudesta kuluraportista, anna raportin syy ja mahdolliset muut käytettävissä olevat tiedot. Nämä tiedot vaihtelevat sen mukaan, miten kulujen hallinta on määritetty yrityksessä.
5. Valitse **Valmis**.
6. Lisää aiemmat kulut, kuten luottokorttitapahtumat, kuluraporttiin valitsemalla **Liitä**.
7. Valitse luettelosta vähintään yksi kulu.
8. Valitse **Valmis**.
9. Lisää uusi kulu kuluraporttiin valitsemalla **Uusi kulu**.
10. Valitse kulun luokka. Näet luettelon kululuokista, jotka on ladattu sovellukseesi offline-käyttöä varten. Oletusarvon mukaan ladataan 50 nimikettä, mutta sovelluskehittäjä voi muuttaa tätä määrää. Sovelluskehittäjille on lisätietoja ohjeaiheessa [Mobiiliympäristö](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md). Jos luokka ei ole luettelossa, tee verkkohaku valitsemalla **Hae**. Etsi kululuokan tai -tyypin perusteella.
11. Valinnainen: anna kulun myyjä.
12. Anna kulun tapahtumapäivämäärä.
13. Syötä kulun summa.
14. Valitse kulun valuutta. Näet luettelon valuuttakoodeista, jotka on ladattu sovellukseesi offline-käyttöä varten. Oletusarvoisesti ladataan 400 valuuttaa, mutta sovelluskehittäjä voi muuttaa tätä määrää. Sovelluskehittäjille on lisätietoja ohjeaiheessa [Mobiiliympäristö](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md). Jos valuutta ei ole luettelossa, tee verkkohaku valitsemalla **Hae**. Etsi valuutan tai nimen mukaan.
15. Valitse **Valmis**.
16. Tarkenna kulun tietoja valitsemalla **Lisää lisätiedot**. Käytettävissä olevat kentät määräytyvät yrityksen kulujen hallinnan määritysten mukaan.
17. Jos yrityksen käytäntö edellyttää kuittien liittämistä, valitse **Kuitit** ja tee seuraavat toimet:

    1. Valitse **Tarkista kuitti** tai **Liitä kuitti**.
    2. Noudata seuraavia ohjeita:

        - Jos valitsit **Tarkista kuitti**, toimi seuraavasti:

            1. Valitse **Ota kuva** tai **Valitse kuva**.
            2. Noudata seuraavia ohjeita:

                - Jos valitsit **Ota kuva** -vaihtoehdon, toimi seuraavasti:

                    1. Sinut siirretään mobiililaitteesi kameraan, jotta voit ottaa kuitista kuvan. Kun olet ottanut kuvan, hyväksy se valitsemalla **OK**.
                    2. Valinnainen: Anna kuvalle nimi ja syötä muistiinpanoja.

                - Jos valitsit **Valitse kuva**, toimi seuraavasti:

                    1. Valitse kuva luettelosta.
                    2. Valinnainen: Anna kuvalle nimi ja syötä muistiinpanoja.

            3.  Valitse **Valmis**.

        - Jos valitsit **Liitä kuitti**, toimi seuraavasti:

            1.  Valitse luettelosta vähintään yksi kuva.
            2.  Valitse **Valmis**.

    3. Palaa kulun tietoihin valitsemalla **Takaisin**.

18. Jos yrityksen käytäntö edellyttää, että kuluun liittyy vieras, valitse **Vierailijat** ja tee seuraavat toimet:

    1. Valitse **Vierailija**, **Aiemmat vieraat** tai **Työtoverit**.
    2. Noudata seuraavia ohjeita:

        - Jos valitsit **Vierailija**, toimi seuraavasti:

            1. Anna vierailijan nimi.
            2. Valinnainen: Annan vierailijan organisaation ja/tai maa.
            3. Valinnainen: Anna vierailijan ammattinimike.
            4. Valitse **Valmis**.

        - Jos valitsit **Aiemmat vieraat**, toimi seuraavasti:

            1. Valitse luettelosta vähintään yksi aiempi vieras. Näkyviin tulee luettelo vieraista, jotka olet lisännyt aiempiin kuluraportteihin. Nämä raportit on ladattu offline-käytön mahdollistavaan sovellukseen. Oletusarvon mukaan ladataan 50 nimikettä, mutta sovelluskehittäjä voi muuttaa tätä määrää. Sovelluskehittäjille on lisätietoja ohjeaiheessa [Mobiiliympäristö](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md). Jos aiempi vieras ei ole luettelossa, tee verkkohaku valitsemalla **Hae**. Voit hakea nimen, organisaation, maan tai ammattinimikkeen perusteella.
            2. Valitse **Valmis**.

        - Jos valitsit **Työtoverit**, toimi seuraavasti:

            1. Valitse luettelosta vähintään yksi työtoveri. Näet luettelon työtovereista, jotka on ladattu sovellukseen offline-käyttöä varten. Oletusarvon mukaan ladataan 50 nimikettä, mutta sovelluskehittäjä voi muuttaa tätä määrää. Sovelluskehittäjille on lisätietoja ohjeaiheessa [Mobiiliympäristö](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md). Jos työtoveri ei ole luettelossa, tee verkkohaku valitsemalla **Hae**. Voit hakea nimen, yrityksen tai ammattinimikkeen perusteella.
            2. Valitse **Valmis**.

    3. Palaa kulun tietoihin valitsemalla **Takaisin**.

19. Jos yrityksen käytäntö edellyttää kulujen erittelyä, valitse **Erittely** ja tee seuraavat toimet:

    1. Valitse erittelyn ensimmäinen päivämäärä.
    2. Valitse **Lisää erittely**.
    3. Valitse kulun erittelyn aliluokka. Näet luettelon kulujen aliluokista, jotka on ladattu sovellukseen offline-käyttöä varten. Oletusarvon mukaan ladataan 50 nimikettä, mutta sovelluskehittäjä voi muuttaa tätä määrää. Sovelluskehittäjille on lisätietoja ohjeaiheessa [Mobiiliympäristö](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md). Jos aliluokka ei ole luettelossa, tee verkkohaku valitsemalla **Hae**. Tee haku kulujen aliluokan nimen mukaan.
    4. Anna eriteltävän tapahtuman summa.
    5. Muokkaa tapahtuman päivämäärää tarvittaessa.
    6. Valitse **Valmis**.
    7. Toista edelliset vaiheet, kunnes kaikki valitun päivämäärän erittelyt on lisätty.
    8. Jos päiviä on enemmän, voit kopioida erittelyt seuraavalle päivälle valitsemalla **Kopioi seuraavaan päivään**. Vaihtoehtoisesti voit valita eriteltävän päivämäärän ja lisätä erittelyt samoin kuin ensimmäisenä päivämääränä.
    9. Kun kulun erittely on valmis, palaa kulun tietoihin valitsemalla **Takaisin**.

20. Palaa **Kuluraportti**-sivulle valitsemalla **Takaisin**.
21. Toista edelliset vaiheet, kunnes kaikki kulut on lisätty.
22. Valitse **Lähetä**.
23. Kirjoita tarvittaessa kommentit hyväksyjälle.
24. Valitse **Valmis**.
