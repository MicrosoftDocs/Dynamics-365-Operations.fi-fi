---
title: 'Perehdytysoppaan luominen ja lähettäminen Dynamics 365 Talent: Onboardin avulla'
description: 'Tässä ohjeaiheessa käsitellään uusien työntekijöiden perehdytysoppaan luontia Microsoft Dynamics 365 Talent: Onboard -sovelluksella. Tämä tehtävä on välttämättömän ensimmäinen vaihe henkilöstöresurssien hallinnan strategiassa joka alkaa työhön ottamisella ja päättyy eläköitymiseen.'
author: andreabichsel
manager: ''
ms.date: 05/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 2371d86165390503312c2848842acf4745a8ed7a
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898245"
---
# <a name="create-and-send-an-onboarding-guide"></a>Perehdytysoppaan luominen ja lähettäminen

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Talent: Onboardilla voi luoda perehdytysoppaita malleista, jotka olet luonut itse tai valikoimassa olevista malleista tai aloittamalla alusta.

Kun olet luonut perehdytysoppaan, voit lähettää sen uudelle työntekijälle. Vaihtoehtoisesti voit lähettää sen niille uusille työntekijöille, jotka olet määrittänyt Onboard-sovelluksesta ladattavaan Microsoft Excel -tiedostoon.

## <a name="create-an-onboarding-guide-from-a-template-and-send-it-to-a-single-new-hire"></a>Perehdytysoppaan luominen mallista ja sen lähettäminen yhdelle uudelle työntekijälle

1. Valitse vasemmassa valikossa **Mallit**.
2. Valitse **Omat mallit** -kohdassa malli, jonka haluat määrittää uuden työntekijän perehdytysoppaaksi.
3. Muokkaa malli sopivaksi. Muista tallentaa tekemäsi muutokset säännöllisesti.
4. Kun mallia ei enää tarvitse muokata, valitse **Luo opas**.

    [![Perehdytysoppaan luominen mallista](./media/onboard-create-guide.png)](./media/onboard-create-guide.png)

5. Anna **Luo opas** -ikkunan **Ketä olet perehdyttämässä?** -kohdassa uuden työntekijän nimi tai sähköpostiosoite. Jos uutta työntekijää ei ole vielä lisätty järjestelmään, valitse **Lisää nyt** ja anna työntekijän tiedot.

    ![[Onboarding-oppaan tietojen syöttäminen](./media/onboard-create-a-guide-window.png)](./media/onboard-create-a-guide-window.png)

6. Valitse **Milloin he aloittavat?** -kohdassa aloituspäivä.
7. Jos perehdytysopas on lähetettävä automaattisesti uudelle työntekijälle tiettynä päivänä, varmista, että **Ajoita automaattinen lähetyspäivämäärä** -vaihtoehto on otettu käyttöön, ja valitse sitten automaattinen lähetyspäivä. Jos haluat lähettää oppaan heti, poista **Ajoita automaattinen lähetyspäivämäärä** -vaihtoehto käytöstä.
8. Valitse **Valmis**.
9. Kun perehdytysopasta ei enää tarvitse muokata, valitse oikeassa yläkulmassa **Lähetä**. Toimi sitten jonkin seuraavien vaiheiden mukaisesti:

    - Voit lähettää linkin perehdytysoppaaseen uudelle työntekijälle valitsemalla ensin **kopioi linkki** ja sitten **Kopioi**.
    - Voit mukauttaa perehdytysoppaan sähköpostiviestiä ennen lähettämistä valitsemalla ensin **Mukauta sähköpostiviestiä ennen lähettämistä** ja sitten **Seuraava**. Mukauta sitten sähköpostiviestiä tarpeen mukaan ja valitse **Lähetä**.
    - Voit lähettää sähköpostiviestin mukauttamatta valitsemalla ensin **Seuraava** ja sitten **Lähetä**.

## <a name="create-an-onboarding-guide-from-a-template-and-send-it-to-multiple-new-hires"></a>Perehdytysoppaan luominen mallista ja sen lähettäminen useille uusille työntekijöille

Onboardissa on mahdollista lähettää perehdytysopas useille uusille työntekijöille samanaikaisesti.

1. Valitse vasemmassa valikossa **Mallit**.
2. Valitse **Omat mallit** -kohdassa malli, jonka haluat määrittää uusien työntekijöiden perehdytysoppaaksi.
3. Muokkaa malli sopivaksi. Muista tallentaa tekemäsi muutokset säännöllisesti.
4. Kun mallia ei enää tarvitse muokata, valitse **Luo opas**.
5. Valitse **Luo opas** -ikkunassa **Oletko perehdyttämässä useita henkilöitä yhtä aikaa?**.

    [![Perehdytysoppaan luominen useille uusille työntekijöille](./media/onboard-send-guide-multiple-people.png)](./media/onboard-send-guide-multiple-people.png)

6. Valitse **uusi työhönottomalli**.
7. Kun .xlsx-tiedosto on ladattu, valitse **Avaa**, anna työntekijöiden tiedot Excel-työkirjassa ja tallenna työkirja.

    [![Excel-mallin lataaminen perehdytysoppaan lähettämiseksi useille uusille työntekijöille](./media/onboard-send-guide-download-spreadsheet.png)](./media/onboard-send-guide-download-spreadsheet.png)

    > [!NOTE]
    > Et voi muokata työkirjaa, ennen kuin valitset Excelissä **Ota muokkaus käyttöön**.
    > 
    > [![Muokkauksen ottaminen käyttöön](./media/onboard-send-guide-enable-editing.png)](./media/onboard-send-guide-enable-editing.png)

8. Vedä Excel-työkirja sille varatulle alueelle **Luo useita oppaita** -ikkunassa tai napsauta tätä aluetta ja hae tiedosto tietokoneessa.

    [![Muokatun työkirjan vetäminen](./media/onboard-send-guide-drag-spreadsheet.png)](./media/onboard-send-guide-drag-spreadsheet.png)

9. Kun perehdytysopasta ei enää tarvitse muokata, valitse oikeassa yläkulmassa **Lähetä**. Toimi sitten jonkin seuraavien vaiheiden mukaisesti:

    - Voit lähettää linkin perehdytysoppaaseen uusille työntekijöille valitsemalla ensin **kopioi linkki** ja sitten **Kopioi**.
    - Voit mukauttaa perehdytysoppaan sähköpostiviestiä ennen lähettämistä valitsemalla ensin **Mukauta sähköpostiviestiä ennen lähettämistä** ja sitten **Seuraava**. Mukauta sitten sähköpostiviestiä tarpeen mukaan ja valitse **Lähetä**.
    - Voit lähettää sähköpostiviestin mukauttamatta valitsemalla ensin **Seuraava** ja sitten **Lähetä**.

## <a name="create-a-guide-without-using-a-template"></a>Oppaan luonti ilman mallia

Opasta ei ole aina pakko luoda mallista. Jos haluat, voit luoda oppaan alusta alkaen.

1. Valitse vasemmassa valikossa ensin **Oppaat** ja sitten **Lisää**-painike (plus-merkki \[**+**\]).
2. Anna **Luo opas** -ikkunan **Ketä olet perehdyttämässä?** -kohdassa uuden työntekijän nimi tai sähköpostiosoite. Jos uutta työntekijää ei ole vielä lisätty järjestelmään, valitse **Lisää nyt** ja anna työntekijän tiedot.

    ![[Onboarding-oppaan tietojen syöttäminen](./media/onboard-create-a-guide-window.png)](./media/onboard-create-a-guide-window.png)

3. Valitse **Milloin he aloittavat?** -kohdassa aloituspäivä.
4. Jos perehdytysopas on lähetettävä automaattisesti uudelle työntekijälle tiettynä päivänä, varmista, että **Ajoita automaattinen lähetyspäivämäärä** -vaihtoehto on otettu käyttöön, ja valitse sitten automaattinen lähetyspäivä. Jos haluat lähettää oppaan heti, poista **Ajoita automaattinen lähetyspäivämäärä** -vaihtoehto käytöstä.
5. Valitse **Valmis**.

## <a name="save-a-guide-as-a-template"></a>Oppaan tallentaminen mallina

Voit tallentaa perehdytysoppaan mallina. Tällä tavoin säästät aikaa, jos sinun on luotava lisää perehdytysoppaita myöhemmin.

1. Valitse vasemmassa valikossa **Oppaat**.
2. Valitse sen oppaan **Lisää**-painike (kolme pistettä \[**...**\]), josta haluat luoda mallin, ja valitse sitten **Tallenna mallina**.

    ![[Onboarding-oppaan tallentaminen mallina](./media/onboard-save-guide-as-template.png)](./media/onboard-save-guide-as-template.png)

3. Anna **Tallenna uutena mallina** -ikkunassa uuden mallin nimi ja valitse sitten **Tallenna**.

## <a name="next-steps"></a>Seuraavat vaiheet

- [Perehdytysoppaiden ja mallien muokkaaminen](./onboard-edit-guides-templates.md)
- [Sisällön jakaminen muiden osallisten kanssa](./onboard-share-template.md)
- [Työntekijöiden tehtävien ja perehdyttämisen tilan näyttäminen](./onboard-view-status.md)
- [Työhönottoryhmien luominen Onboardissa](./onboard-create-team.md)

### <a name="see-also"></a>Lisätietoja

- [Onboard-sovelluksen kokeileminen tai ostaminen](https://dynamics.microsoft.com/talent/onboard/)
- [Dynamics 365 Talentin uudet ja muuttuneet ominaisuudet](./whats-new.md)
- [Julkaisusuunnitelmat](https://docs.microsoft.com/business-applications-release-notes/index)
- [Microsoft iDynamics 365 Talentin tuki](./talent-support.md)
