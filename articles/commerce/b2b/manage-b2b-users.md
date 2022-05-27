---
title: Liikekumppanikäyttäjien hallinta B2B-verkkokauppasivustoissa
description: Tässä aiheessa kuvataan, miten liikekumppanikäyttäjiä lisätään, poistetaan ja muokataan Microsoft Dynamics 365 Commercen yritysten välisillä (B2B) verkkokauppasivustoilla ja Commerce headquarters -sovelluksessa.
author: josaw1
ms.date: 04/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ef8ae583f18048fc6a36adf38ee7be0fb5b02fcd
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686321"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites"></a>Liikekumppanikäyttäjien hallinta B2B-verkkokauppasivustoissa

[!include [banner](../../includes/banner.md)]

Tässä aiheessa kuvataan, miten liikekumppanikäyttäjiä lisätään, poistetaan ja muokataan Microsoft Dynamics 365 Commercen yritysten välisillä (B2B) verkkokauppasivustoilla ja Commerce headquarters -sovelluksessa.

> [!NOTE]
> - Aihe [B2B-liikekumppaneiden hallinta asiakashierarkioiden avulla](partners-customer-hierarchies.md) on edellytys tälle asiakirjalle.
> - Varmista, että alustat Commerce Headquarters -asiakirjatyyppien yksikön avaamalla **Tiedostotyypit**-lomakkeen kohdassa **Organisaation hallinta \> Tiedostojen hallinta \> Asiakirjatyypit**.

B2B-verkkokauppasivustot edellyttävät, että organisaatiot rekisteröityvät liikeyhteistyökumppaneina. Kun organisaatio on lähettänyt rekisteröintitiedot B2B-verkkokauppasivustoon, rekisteröintipyyntö käy läpi hyväksyntäprosessin. Jos organisaatio on hyväksytty onnistuneesti, se on mukana liikekumppanina.

Kun organisaatio on mukana liikekumppanina, liikekumppanipyynnön aloittanut organisaation käyttäjä tunnistetaan järjestelmänvalvojakäyttäjäksi, ja käyttäjälle myönnetään oikeudet lisätä muita valtuutettuja käyttäjiä B2B-verkkokauppasivuston. Hyväksytyt käyttäjät voivat sitten tehdä tilauksia liikekumppanin puolesta.

## <a name="set-up-the-administrator-user-for-a-new-business-partner"></a>Järjestelmänvalvojakäyttäjän määrittäminen uudelle liikekumppanille

Mahdolliset liikekumppanit voivat käynnistää käyttöönottoprosessin B2B-verkkokauppasivustolle lähettämällä käyttöönottopyynnön B2B-verkkosivuston linkin kautta. Sen jälkeen he voivat käyttää mukautettavaa lomaketta käyttöönottoon ja rekisteröitymiseen vaadittavien tietojen antamiseen. Kun pyyntö on lähetetty, näkyviin tulee lähetysvahvistussivu. Jos lähetys hyväksytään, yrityksestä, jonka osalta pyyntö on lähetetty, tulee liikekumppani ja pyytäjästä (pyynnön käynnistänyt käyttäjä) tulee liikekumppanin järjestelmänvalvojakäyttäjä.

Liikekumppanipyynnöt hyväksytään Commerce headquarters -sovelluksessa seuraavien ohjeiden mukaisesti.

1. Siirry kohtaan **Vähittäismyynnin IT \> Jakeluaikataulu**.
1. Aja **P-0001**-työ, kun haluat vetää kaikki liikekumppanipyynnöt Commerce headquartersiin.
1. Kun **P-0001**-työ on suoritettu onnistuneesti, siirry kohtaan **Retail ja Commerce IT \> Asiakas** ja suorita **Synkronoi asiakkaat ja kanavapyynnöt** -työ. Kun tämä työ on suoritettu onnistuneesti, käyttöönottopyynnöt luodaan Commerce headquarters **B2B-prospekti**-tyypin prospekteina. 
1. Siirry kohtaan **Asiakkaat \> Kaikki prospektit** ja avaa prospektin tietosivu valitsemalla uuden liikekumppaniprospektitietue.
1. Hyväksy tarjouspyyntö valitsemalla **Yleiset**-välilehdessä **Muunna \> Hyväksy tai hylkää**. Kun vahvistussanoma tulee näyttöön, vahvista, että haluat jatkaa prosessia, ja hyväksy pyyntö. Hyväksyminen muuttaa prospektitietueen **Tila**-arvoksi **Hyväksytty**. Tämän jälkeen sähköposti lähetetään pyytäjän sähköpostiosoitteeseen, joka vahvistaa, että heidän organisaationsa on hyväksytty liikekumppaniksi. Tässä luodaan myös asiakashierarkia, jossa pyytäjä lisätään liikekumppanin järjestelmänvalvojaksi.

    > [!NOTE]
    > Tällä hetkellä vahvistussähköpostiviesti lähetetään välittömästi hyväksymisen jälkeen. Tulevissa Commerce-toiminnoissa järjestelmänvalvoja kuitenkin voi käynnistää sähköpostiviestit manuaalisesti.

1. Siirry kohtaan **Retail ja Commerce IT \> Jakeluaikataulu** ja suorita työ **1010 (Asiakkaat)** työntääksesi uudet asiakas- ja asiakashierarkiatietueet kanavatietokantaan.

> [!NOTE]
> Jotta voidaan varmistaa, että uudet asiakastietueet lähetetään kanavatietokantaan, vähintään yhden asiakkaaseen liitetyistä osoitekirjoista on sisällyttävä verkkokauppaan liittyvään asiakasosoitekirjaan. Voit automatisoida tämän prosessin määrittämällä verkkokaupan oletusasiakkaan osoitekirjan siten, että järjestelmä kopioi osoitekirjan arvon jokaiselle uudelle asiakkaalle.

Kun asiakashierarkiatietueet synkronoidaan kanavatietokantaan, pyytäjä voi kirjautua B2B-verkkokauppasivustoon käyttäen heidän käyttöönottopyynnön mukana toimittamaansa sähköpostiosoitetta. Käyttäjät voivat kirjautumisvirran avulla määrittää tilinsä salasanan. Tietoja Azure Active Directoryn (Azure AD:n) B2C-tunnuksen tarjoajan tietueen linkittämisestä prospektin hyväksymisen yhteydessä luotuun B2B-asiakastietueeseen: [Automaattisen linkityksen käyttöönotto](../identity-record-linking.md).

## <a name="notify-b2b-prospects-when-they-are-approved-or-rejected"></a>B2B-prospekteille ilmoittaminen, kun heidät on hyväksytty tai hylätty

Kun hyväksyt tai hylkäät B2B-prospektin aktivointipyynnön, prospektille voidaan lähettää automaattisesti sähköposti-ilmoitus.

Voit määrittää Commerce-pääkonttorisovelluksessa sähköposti-ilmoituksia ilmoitustyypin **B2B-prospekti hyväksytty** tai **B2B-prospekti hylätty** tapahtumalle seuraavalla tavalla.

1. Luo sähköpostimalleja prospekteille lähetettäville sähköposteille, kun joko ilmoitustyyppi **B2B-prospekti hyväksytty** tai **B2B-prospekti hylätty** käynnistyy. Lisätietoja paikkamerkeistä, joita ilmoitustyypit tukevat: [Ilmoitustyypit](../email-templates-transactions.md#notification-types). Tietoja sähköpostimallien luonnista: [Sähköpostimallin luonti](../email-templates-transactions.md#create-an-email-template).
1. Lisää ilmoitustyypit **B2B-prospekti hyväksytty** tai **B2B-prospekti hylätty** sähköposti-ilmoitusprofiilisi ja yhdistä ne sitten luomiisi sähköpostimalleihin. Lisätietoja ilmoitusprofiileista: [Määritä sähköposti-ilmoitusprofiili](../email-notification-profiles.md).

## <a name="onboard-additional-business-partner-users"></a>Lisäliikekumppanikäyttäjien perehdyttäminen

Liikekumppanin järjestelmänvalvojakäyttäjä voi tarvittaessa lisätä liikekumppanikäyttäjiä B2B-verkkokauppasivustoon.

Noudattamalla seuraavia ohjeita voit ottaa lisäliikekumppanikäyttäjiä mukaan B2B-verkkokauppasivustoon.

1. Kirjaudu sisään B2B-verkkokauppasivustoon järjestelmänvalvojana.
1. Siirry kohtaan **Oma tili \> Organisaation käyttäjät \> Näytä tiedot** ja valitse **Lisää käyttäjä**.
1. Syötä tarvittavat tiedot ja valitse sitten **Tallenna**. Uuden käyttäjän tilakentän asetuksena on **Odottaa**.

Kun työt **P-0001** ja **Synkronoi asiakkaat ja kanavoi pyynnöt** on suoritettu, uudelle käyttäjälle luodaan **Henkilö**-tyypin asiakastietue Commerce headquarters -sovelluksessa. Tämä asiakastietue liittyy myös liikekumppanin asiakashierarkiatietueeseen. Lisäksi sähköposti lähetetään uuden käyttäjän sähköpostiosoitteeseen, joka ilmoittaa, että heidät on lisätty liikekumppaniorganisaation käyttäjänä ja voivat nyt kirjautua B2B-verkkokauppasivustoon.

Synkronoi sitten uusi liikekumppanin käyttäjä kanavatietokantaan suorittamalla työ **1010 (Asiakkaat)**.

Kun asiakastietue on synkronoitu, B2B-verkkokauppasivuston käyttäjän tilaksi tulee **Aktiivinen**, ja uusi käyttäjä voi kirjautua B2B-verkkokauppasivustoon sähköpostiosoitteensa avulla. Käyttäjät voivat kirjautumisvirran avulla määrittää tilinsä salasanan. Tietoja Azure AD:n B2C-tunnuksen tarjoajan tietueen linkittämisestä Commerce headquarters -sovelluksessa luotuun B2B-asiakastietueeseen: [Automaattisen linkityksen käyttöönotto](/dynamics365/commerce/identity-record-linking.md).

## <a name="edit-business-partner-user-details"></a>Liikekumppanikäyttäjän tietojen muokkaaminen

Jos haluat muokata liikekumppanikäyttäjien tietoja, noudata seuraavia ohjeita.

1. Kirjaudu sisään B2B-verkkokauppasivustoon järjestelmänvalvojana.
1. Siirry kohtaan **Oma tili \> Organisaation käyttäjät \> Näytä tiedot**, valitse **Muokkaa**-painike (kynäsymboli), tee tarvittavat muutokset ja valitse **Tallenna**. Muutokset tulevat voimaan vasta, kun työ **P-0001**, **Synkronoi asiakkaat ja kanavoi pyynnöt** ja **1010 (Asiakkaat)** on suoritettu.

## <a name="remove-a-business-partner-user"></a>Liikekumppanikäyttäjän poistaminen

Järjestelmänvalvoja voi tarvittaessa poistaa liikekumppaniorganisaation olemassa olevia käyttäjiä niiden käyttäjien luettelosta, jotka voivat käyttää B2B-verkkokauppasivustoa.
Jos haluat poistaa liikekumppanikäyttäjän, noudata seuraavia ohjeita.
- Kirjaudu sisään B2B-verkkokauppasivustoon järjestelmänvalvojana.
- Siirry kohtaan **Oma tili > Organisaation käyttäjät \> Näytä tiedot** ja valitse **Poista**-painike (X-symboli). Kun näkyviin tulee vahvistussanoma, vahvista, että haluat poistaa käyttäjän. Muutos tulee voimaan vasta, kun työ **P-0001**, **Synkronoi asiakkaat ja kanavoi pyynnöt** ja **1010 (Asiakkaat)** on suoritettu.

> [!NOTE]
> Kun poistat käyttäjän niiden käyttäjien luettelosta, jotka voivat käyttää B2B-verkkokauppasivustoa, vastaava asiakastietue poistetaan liikekumppanin asiakashierarkiatietueesta. Asiakastietuetta ei kuitenkaan poisteta Commerce headquartersista.

## <a name="onboard-existing-customers-as-business-partners-on-the-b2b-e-commerce-website"></a>Ota olemassa olevat asiakkaat käyttöön liikekumppaneina B2B-verkkokauppasivustolla.

Järjestelmänvalvojat voivat ottaa käyttöön liikekumppaneita ja käyttäjia suoraan Commerce headquarters -sovelluksessa. Tämä ominaisuus on hyödyllinen, kun olemassa olevia liikekumppaneita otetaan käyttöön B2B-verkkokauppasivustolla.

Voit ottaa käyttöön liikekumppaneita ja käyttäjia Commerce headquarters -sovelluksessa seuraavasti.

1. Luo tai valitse **Organisaatio**-tyypin asiakas lisättäväksi liikekumppanina.
1. Luo tai valitse **Henkilö**-tyypin asiakas lisättäväksi liikekumppanin järjestelmänvalvojana tai käyttäjänä. Varmista, että asiakkailla on ensisijaiset sähköpostiosoitteet. Näitä sähköpostiosoitteita käytetään verkkosivustolle kirjautumisessa. 

    > [!NOTE]
    > Järjestelmän on kyettävä löytämään yksilöllinen asiakastietue käyttäjille, joiden pitäisi pystyä kirjautumaan verkkosivustolle. Jos järjestelmä löytää useamman kuin yhden asiakkaan, jolla on sama ensisijainen sähköpostiosoite, käyttäjä ei voi kirjautua verkkosivustolle.

1. Luo asiakashierarkian tunnus.
1. Anna nimi **Nimi**-kenttään.
1. Syötä **Organisaatio**-kentässä liikekumppaniorganisaatioasiakas.
1. Valitse **Hierarkia**-pikavälilehdessä **Lisää**.
1. Valitse **Nimi**-kentässä **Henkilö**-tyypin asiakas.
1. Valitse järjestelmänvalvojaksi määritettävälle asiakkaalle **Järjestelmänvalvoja**-rooli.
1. Toista tämä prosessi, kun haluat lisätä hierarkiaan muita asiakkaita.

## <a name="additional-information"></a>Lisätiedot

- Kaikki tässä ohjeaiheessa mainitut työt voidaan konfiguroida suoritettavaksi aikataulussa erämuodossa. Odotus on se, että liikekumppanit konfiguroivat erätyöt tarpeen mukaan.
- Järjestelmänvalvojakäyttäjäksi voidaan määrittää tällä hetkellä vain yksi käyttäjä tai asiakastietue, ja tätä roolia voi muuttaa vain Commerce headquarters -sovelluksessa. Ei ole tukea itsepalvelutoiminnoille, joilla liikekumppanit voivat määrittää useita järjestelmänvalvojia tai muuttaa B2B-verkkokauppasivustojen järjestelmänvalvojia.
- Vaikka käyttäjille voidaankin määrittää kulutuksen rajat, kulutuksen rajojen pakottamista tilaustenkäsittelyprosessin aikana ei ole vielä otettu käyttöön.
- Kaikki käyttäjäkokemuksen liiketoimintalogiikka ja oikeellisuustarkistus B2B-verkkokauppasivustossa perustuu sen asiakastietueen konfigurointiin, joka on yhdistetty Commerce headquarters -sovelluksen käyttäjään.

## <a name="additional-resources"></a>Lisäresurssit

[Yritystenvälisen yhteistyön sähköisen kaupankäynnin sivuston määrittäminen](set-up-b2b-site.md)

[B2B-liikekumppaneiden hallinta asiakashierarkioiden avulla](partners-customer-hierarchies.md)

[Asiakastilin maksutavan määrittäminen B2B-verkkokauppasivustoille](payment-method.md)

[Tuotemäärän rajojen asettaminen B2B-verkkokauppasivustoille](quantity-limits.md)

[Numerosarjojen yleiskatsaus](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
