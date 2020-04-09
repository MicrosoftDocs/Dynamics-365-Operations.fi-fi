---
title: Kulutositteiden käsittely
description: Tässä ohjeaiheessa on tietoja optisen merkkien tunnistuksen (OCR) käytöstä tositteiden käsittelyssä. Tämä ominaisuus on suunniteltu parantamaan käyttökokemusta, kun luodaan kuluraportteja Microsoft Dynamics 365 Financessa.
author: stsporen
manager: AnnBe
ms.date: 11/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 49cdfeac8cda9f1ddd3aca61f902f00f30f3485b
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154037"
---
# <a name="expense-receipt-processing"></a>Kulukuittien käsittely

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Kulujen kirjausta on parannettu ottamalla käyttöön optinen merkkien tunnistus (OCR) tositteiden osalta. Tämä ominaisuus on suunniteltu parantamaan käyttökokemusta, kun luodaan kuluraportteja.

## <a name="key-features"></a>Tärkeimmät ominaisuudet

- Tositteista haetaan myyjän nimi, päivämäärä ja kokonaissumma.
- Ominaisuus yrittää yhdistää liittämättömät tositteet liittämättömiin kulutapahtumiin.
- Käyttäjät voivat luoda tositteista manuaalisesti kirjattuja kulutapahtumia.

## <a name="usage-examples"></a>Käyttöesimerkkejä

- **Luottokorttitapahtumia sisältävien tositteiden automaattinen liittäminen, kun kuluraportti luodaan.**

    1. Avaa **Kulujen hallinta** -työtila.
    2. Tarkista **Tositteet**-välilehdessä, että liittämättömiä tositteita on olemassa. Voit myös ladata tositteita **Tositteet**-välilehteen.
    3. Tarkista **Kulut**-välilehdessä, että liittämättömiä kuluja on olemassa. Tavallisesti kulujen hallinnoija tuo nämä kulut luottokortin myöntäjältä.
    4. Valitse **Uusi kuluraportti**. Huomaa, että voit nyt sisällyttää kuluja ja tositteita myös kuluraporttiin. Jos lisäät sekä kuluja että tositteita, automaattinen tositteiden ja kulujen yhdistäminen käynnistyy.

- **Luo kulu tai yhdistä kulu tositteesta.**

    1. Liitä tosite kuluraporttiin valitsemalla sen **Tositteet**-välilehdessä **Lisää tositteita**.
    2. Huomaa tositteen ladatun kuvan alla asetukset **Luo** ja **Yhdistä**.

        - Luo manuaalisesti kirjattu kulutapahtuma ja täytä tositteesta haetut arvot valitsemalla **Luo**.
        - Jos valitset **Yhdistä**, järjestelmä yrittää yhdistää olemassa olevan kulun tositteeseen.

## <a name="installation"></a>Asentaminen

Tämä ominaisuus toimii yhdessä **Kuluraporttien uusi toteutus** -ominaisuuden kanssa yksinkertaistaen kulukokemusta.

Jos haluat käyttää näitä kehittyneitä kuluominaisuuksia, asenna Microsoftin Dynamics 365 Financen kulujenhallintapalvelu ja ota ominaisuudet käyttöön esiintymässäsi. Voit käyttää lisäosaa projektistasi Microsoft Dynamicsin Lifecycle Servicesissä (LCS).

1. Kirjaudu sisään LCS:ään ja avaa sopiva ympäristö.
2. Valitse **Kaikki tiedot**.
3. Valitse **Ylläpito** tai selaa alas **Ympäristön lisäosat** -pikavälilehteen.
4. Valitse **Asenna uusi lisäosa**.
5. Valitse **Kulujenhallintapalvelu**.
6. Noudata asennusoppaan ohjeita ja hyväksy käyttöehdot.
7. Valitse **Asenna**.

Ota **Ominaisuuksien hallinta** -työtilassa käyttöön seuraavat ominaisuudet:

- Kuluraporttien uusi toteutus
- Automaattinen vastaavuus ja kulujen luonti kuitista

Kun otat nämä ominaisuudet käyttöön, seuraavat toiminnot toteutuvat:

- Aiemmin luotu **Kulujen hallinta** -työtila korvataan uudella työtilalla.
- Uusi kulukentän näkyvyyden valikkovaihtoehto lisätään.
- Voit edelleen avata aiemman **Kuluraportit** -sivun siirtymällä kohtaan **Kulujen hallinta > Omat kulut > Kuluraportit**.
- Työn kulut ja hyväksynnät ovat edelleen olemassa kuluraportit-sivulla.
- Tositteet käsitellään Microsoft Azure Cognitive Servicesin kautta ja metatietoja haetaan ja lisätään.
- Järjestelmä lisää vaihtoehdon, jonka avulla voit luoda kuluraportin, joka sisältää yhdistetyt liittämättömät tositteet.
- Kuluraportteihin lisättävä vaihtoehto mahdollistaa kulurivin luomisen tositteesta. Se voi myös yrittää yhdistää olemassa olevan tositteen olemassa olevaan kuluriviin.

Lisätietoja Kuluraporttien uusi toteutus -ominaisuudesta on kohdassa [Kuluraporttien uusi toteutus](ExpenseWorkspaceNew.md)

## <a name="frequently-asked-questions"></a>Usein kysytyt kysymykset

**Käyttääkö Microsoft tietojani mallejaan varten?**

Ei, Microsoft kehittänyt yleisen koneoppimismallin tositteiden käsittelypalveluaan varten. Tämä malli ei perustu lataamiisi tositteisiin.

**Missä tämä ominaisuus on käytettävissä ja missä se käsitellään?**

Tällä hetkellä tuettuna on Yhdysvallat.

**Minne tositteeni menevät?**

Finance muodostaa yhteyden Cognitive Servicesiin hakeakseen kenttätiedot. Cognitive Services säilyttää kopion tositteestasi käsittelyn yhteydessä jopa 24 tunnin ajan. Kun käsittely on valmis, Cognitive Services poistaa tositteen. Tositteet ovat edelleen tallennettuna Financessa.

Lisätietoja on kohdassa [Ota käyttöön tositteiden käsittely muodontunnistimen uudella ominaisuudella](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).
