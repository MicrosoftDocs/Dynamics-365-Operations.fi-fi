---
title: Liikekumppanikäyttäjien hallinta B2B-verkkokauppasivustoissa
description: Tässä aiheessa kuvataan, kuinka järjestelmänvalvojat voivat lisätä, muokata ja poistaa yritysten välisten (B2B) verkkokauppasivustojen liikekumppanikäyttäjiä.
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9cd1e3e38bf7dd5ac536104c850cbfc6c53abcfd
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211246"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites"></a>Liikekumppanikäyttäjien hallinta B2B-verkkokauppasivustoissa

[!include [banner](../../includes/banner.md)]

Tässä aiheessa kuvataan, kuinka järjestelmänvalvojat voivat lisätä, muokata ja poistaa yritysten välisten (B2B) verkkokauppasivustojen liikekumppanikäyttäjiä.

B2B-verkkokauppasivustot edellyttävät, että organisaatiot rekisteröityvät liikeyhteistyökumppaneina. Kun organisaatio on lähettänyt rekisteröintitiedot B2B-verkkokauppasivustoon, se käy läpi hyväksyntäprosessin. Jos organisaatio on hyväksytty onnistuneesti, se on mukana liikekumppanina.

Kun organisaatio on mukana liikekumppanina, liikekumppanipyynnön aloittanut organisaation käyttäjä tunnistetaan järjestelmänvalvojakäyttäjäksi, ja käyttäjälle myönnetään oikeudet lisätä muita valtuutettuja käyttäjiä B2B-verkkokauppasivuston. Hyväksytyt käyttäjät voivat sitten tehdä tilauksia liikekumppanin puolesta.

## <a name="turn-on-the-b2b-e-commerce-capabilities-feature-in-commerce-headquarters"></a>B2B-verkkokaupan ominaisuuden käyttöönotto Commerce headquarters -sovelluksessa

Commerce headquartersin B2B-verkkokauppaominaisuus mahdollistaa organisaatioiden ottaa mukaan liikekumppaneita ja määrittää järjestelmänvalvojakäyttäjiä. Tämän toiminnon avulla järjestelmänvalvojat voivat myös luoda ja hallita liikekumppanien käyttäjiä ja ryhmiä sekä määrittää heille rooleja. Lisäksi liikekumppanien käyttäjät voivat luoda tilausmalleja ja käyttää olemassa olevia tilauksia tuotteiden uudelleen tilaamiseen.

Ota B2B-verkkokaupan ominaisuus käyttöön Commerce headquarters -sovelluksessa seuraavien ohjeiden mukaan.

1. Valitse **Työtilat \> Ominaisuuden hallinta**.
1. Suodata **Kaikki**-välilehden **Moduuli**-kentän arvolla **Retail ja Commerce**.
1. Etsi ja valitse toiminto, jonka nimi on **Ota käyttöön B2B-verkkokauppaominaisuudet**, ja valitse sitten **Ota käyttöön nyt**.

## <a name="create-a-number-sequence-and-add-it-to-commerce-shared-parameters"></a>Numerosarjan luominen ja sen lisääminen Commercen jaettuihin parametreihin

Numerosarjoilla luodaan luettavia, yksilöllisiä tunnisteita niitä edellyttäville päätietojen tietueille ja tapahtumatietueille. Lisätietoja numerosarjoista on kohdassa [Numerosarjojen yleiskatsaus](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview).

Voit luoda numerosarjan ja lisätä sen Commercen jaetuille parametreille Commerce headquarters -sovelluksessa noudattamalla seuraavia vaiheita.

1. Siirry kohtaan **Retail ja Commerce \> Headquartersin asetukset \> Numerosarjat \> Numerosarjat** ja luo numerosarja.
1. Siirry kohtaan **Retail ja Commerce \> Headquartersin asetukset \> Parametrit \> Commercen jaetut parametrit** ja lisää uusi numerosarja **Asiakashierarkian tunnus** -viitteeseen.

## <a name="set-up-the-administrator-user-for-a-new-business-partner"></a>Järjestelmänvalvojakäyttäjän määrittäminen uudelle liikekumppanille

Mahdolliset liikekumppanit voivat käynnistää käyttöönottoprosessin B2B-verkkokauppasivustolle lähettämällä käyttöönottopyynnön sivuston linkin kautta. Kun potentiaalinen liikekumppanikäyttäjä valitsee linkin, hän voi antaa rekisteröitymisen ja käytön edellyttämät tiedot. Kun pyyntö on lähetetty, näkyviin tulee lähetysvahvistussivu. Jos lähetys on hyväksytty, pyytäjästä (pyynnön käynnistänyt käyttäjä) tulee liikekumppanin järjestelmänvalvojakäyttäjäksi.

Noudattamalla seuraavia ohjeita voit hyväksyä ja määrittää liikekumppanin järjestelmänvalvojakäyttäjän Commerce headquarters -sovelluksessa.

1. Siirry kohtaan **Vähittäismyynnin IT \> Jakeluaikataulu**.
1. Aja **P-0001**-työ, kun haluat vetää kaikki liikekumppanipyynnöt Commerce headquartersiin.
1. Kun **P-0001**-työ on suoritettu onnistuneesti, siirry kohtaan **Vähittäismyynnin IT \> Asiakas** ja suorita **Synkronoi asiakkaat ja yrityskumppanit asynkronisesta tilasta** -työ. Kun tämä työ on suoritettu onnistuneesti, käyttöönttopyynnöt luodaan Commerce headquarters -prospektitietueena. Näiden tietueiden **Tyyppitunnus**-kentän arvona on **B2B-prospekti**.
1. Siirry kohtaan **Asiakkaat \> Kaikki prospektit** ja avaa prospektisivu.
1. Avaa prospektin tietosivu valitsemalla uuden liikekumppanin prospektitietue.
1. Hyväksy tai hylkää tarjouspyyntö valitsemalla **Yleiset**-välilehdessä **Muunna \> Hyväksy tai hylkää**. Kun vahvistussanoma tulee näyttöön, vahvista, että haluat jatkaa prosessia, ja hyväksy pyyntö. Tämän jälkeen sähköposti lähetetään pyytäjän sähköpostiosoitteeseen, joka vahvistaa, että heidän organisaationsa on hyväksytty liikekumppaniksi.

    Kun olet hyväksynyt pyynnön, prospektitietueen **Tila**-arvoksi tulee **Hyväksytty**. Järjestelmään luodaan myös kaksi uutta asiakastietuetta: liikekumppaniorganisaation **Tyyppi – organisaatio** -asiakastietue ja pyytäjän **Tyyppi – henkilö** -asiakastietue. Myös liikekumppanin asiakashierarkiatietue luodaan. <!--(Please refer to the Org modeling of B2B customer section in this document for more information)-->

1. Siirry kohtaan **Retail ja Commerce IT \> Jakeluaikataulu** ja suorita työ **1010** (**Asiakkaat**) työntääksesi uudet asiakas- ja asiakashierarkiatietueet kanavatietokantaan.

Kun pyyntö on hyväksytty ja asiakas- ja asiakashierarkiatietueet synkronoidaan kanavatietokantaan, pyytäjä voi kirjautua B2B-verkkokauppasivustoon käyttäen heidän pyynnön mukana toimittamaansa sähköpostiosoitetta. Käyttäjät voivat kirjautumisvirran avulla määrittää tilinsä salasanan.

## <a name="onboard-additional-business-partner-users"></a>Lisäliikekumppanikäyttäjien perehdyttäminen

Liikekumppanin järjestelmänvalvojakäyttäjä voi tarvittaessa lisätä liikekumppanikäyttäjiä B2B-verkkokauppasivustoon.

Noudattamalla seuraavia ohjeita voit ottaa lisäliikekumppanikäyttäjiä mukaan B2B-verkkokauppasivustoon.

1. Kirjaudu sisään B2B-verkkokauppasivustoon järjestelmänvalvojana.
1. Siirry kohtaan **Oma tili \> Organisaation käyttäjät \> Näytä tiedot** ja valitse **Lisää käyttäjä**.
1. Syötä tarvittavat tiedot ja valitse sitten **Tallenna**. Uuden käyttäjän tilakentän asetuksena on **Odottaa**.

    Kun työt **P-0001** ja **Synkronoi asiakkaat ja yrityskumppanit asynkronisesta tilasta** suoritetaan, uudelle käyttäjälle luodaan **Tyyppi – henkilö** -asiakastietue Commerce headquarters -sovelluksessa. Tämä asiakastietue liittyy myös liikekumppanin asiakashierarkiatietueeseen. Lisäksi sähköposti lähetetään uuden käyttäjän sähköpostiosoitteeseen, joka ilmoittaa, että heidät on lisätty liikekumppaniorganisaation käyttäjänä ja voivat nyt kirjautua B2B-verkkokauppasivustoon.

1. Synkronoi uusi liikekumppanin käyttäjä kanavatietokantaan suorittamalla työ **1010** **(Asiakkaat)**.

Kun asiakastietue on synkronoitu, B2B-verkkokauppasivuston käyttäjän tilaksi tulee **Aktiivinen**, ja uusi käyttäjä voi kirjautua B2B-verkkokauppasivustoon sähköpostiosoitteensa avulla. Käyttäjät voivat kirjautumisvirran avulla määrittää tilinsä salasanan.

## <a name="edit-business-partner-user-details"></a>Liikekumppanikäyttäjän tietojen muokkaaminen

Jos haluat muokata liikekumppanikäyttäjien tietoja, noudata seuraavia ohjeita.

1. Kirjaudu sisään B2B-verkkokauppasivustoon järjestelmänvalvojana.
1. Siirry kohtaan **Oma tili \> Organisaation käyttäjät \> Näytä tiedot**, valitse **Muokkaa**-painike (kynäsymboli), tee tarvittavat muutokset ja valitse **Tallenna**. Muutokset tulevat voimaan vasta, kun työ **P-0001**, **Synkronoi asiakkaat ja yrityskumppanit asynkronisesta tilasta** ja **1010** (**Asiakkaat**) on suoritettu.

## <a name="remove-a-business-partner-user"></a>Liikekumppanikäyttäjän poistaminen

Järjestelmänvalvoja voi tarvittaessa poistaa liikekumppaniorganisaation olemassa olevia käyttäjiä niiden käyttäjien luettelosta, jotka voivat käyttää B2B-verkkokauppasivustoa.

Jos haluat poistaa liikekumppanikäyttäjän, noudata seuraavia ohjeita.

1. Kirjaudu sisään B2B-verkkokauppasivustoon järjestelmänvalvojana.
1. Siirry kohtaan **Oma tili \> Organisaation käyttäjät \> Näytä tiedot** ja valitse **Poista**-painike (X-symboli). Kun näkyviin tulee vahvistussanoma, vahvista, että haluat poistaa käyttäjän. Muutos tulee voimaan vasta, kun työ **P-0001**, **Synkronoi asiakkaat ja yrityskumppanit asynkronisesta tilasta** ja **1010** (**Asiakkaat**) on suoritettu.

> [!NOTE]
> Kun poistat käyttäjän niiden käyttäjien luettelosta, jotka voivat käyttää B2B-verkkokauppasivustoa, vastaava asiakastietue poistetaan liikekumppanin asiakashierarkiatietueesta. Asiakastietuetta ei kuitenkaan poisteta Commerce headquartersista.

## <a name="onboard-business-partner-and-users-in-commerce-headquarters"></a>Ota liikekumppaneita ja käyttäjiä käyttöön ja Commerce headquartersissa

Järjestelmänvalvojat voivat ottaa käyttöön liikekumppaneita ja käyttäjia suoraan Commerce headquarters -sovelluksessa.

Voit ottaa käyttöön liikekumppaneita ja käyttäjia Commerce headquarters -sovelluksessa seuraavasti.

1. Luo **Tyyppi – organisaatio** -asiakastietue liikekumppaniorganisaatiolle.
1. Luo **Tyyppi – henkilö** -asiakastietueita liikekumppanikäyttäjille. Varmista, että jokaiselle asiakkaalle on määritetty ensisijainen sähköpostiosoite.
1. Määritä **Vähittäismyynti**-pikavälilehdissä **B2B-järjestelmänvalvoja**-asetukseksi **Kyllä** kullekin **Tyyppi – henkilö** -asiakastietueelle, joka on määritettävä liikekumppaniorganisaation järjestelmänvalvojakäyttäjänä.
1. Luo asiakashierarkian tunnus. Anna nimi **Nimi**-kenttään.
1. Syötä **Organisaatio**-kentässä liikekumppaniorganisaatioasiakas.
1. Valitse **Lisää** ja sitten **Nimi**-kentässä asiakas.
1. Toista tämä prosessi, kun haluat lisätä hierarkiaan muita asiakkaita.

## <a name="additional-information"></a>Lisätiedot

- Kaikki tässä ohjeaiheessa mainitut työt voidaan konfiguroida suoritettavaksi aikataulussa erämuodossa. Odotus on se, että liikekumppanit konfiguroivat erätyöt tarpeen mukaan.
- Järjestelmänvalvojakäyttäjäksi voidaan määrittää tällä hetkellä vain yksi käyttäjä tai asiakastietue, ja tätä roolia voi muuttaa vain Commerce headquarters -sovelluksessa. Ei ole tukea itsepalvelutoiminnoille, joilla liikekumppanit voivat määrittää useita järjestelmänvalvojia tai muuttaa B2B-verkkokauppasivustojen järjestelmänvalvojia.
<!--- The modules and labels of the different fields referenced in the screenshots for e-commerce are only for illustration purposes. Customers have complete control on the placement of the B2B related modules and the labels.-->
- Vaikka käyttäjille voidaankin määrittää kulutuksen rajat, kulutuksen rajojen pakottamista tilaustenkäsittelyprosessin aikana ei ole vielä otettu käyttöön.
- Kaikki käyttäjäkokemuksen liiketoimintalogiikka ja oikeellisuustarkistus B2B-verkkokauppasivustossa perustuu sen asiakastietueen konfigurointiin, joka on yhdistetty Commerce headquarters -sovelluksen käyttäjään.

## <a name="additional-resources"></a>Lisäresurssit

[B2B-verkkokauppasivuston määrittäminen](set-up-b2b-site.md)

[Organisaation mallinnushierarkioiden luominen B2B-organisaatioille](org-model.md)

[Asiakastilin maksutavan määrittäminen B2B-verkkokauppasivustoille](payment-method.md)

[Tuotemäärän rajojen asettaminen B2B-verkkokauppasivustoille](quantity-limits.md)

[Numerosarjojen yleiskatsaus](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]