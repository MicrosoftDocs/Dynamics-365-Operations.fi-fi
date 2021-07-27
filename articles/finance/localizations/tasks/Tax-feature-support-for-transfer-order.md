---
title: Siirtotilausten verotoiminnon tuki
description: Tässä aiheessa kuvataan siirtotilausten uutta verotoimintoa veron laskentapalvelua käyttäen.
author: kailiang
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 7b97eca8c2d4fe9f71c3cd8f1e40a3bbb7ee4879
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/06/2021
ms.locfileid: "6348413"
---
# <a name="tax-feature-support-for-transfer-orders"></a>Siirtotilausten verotoiminnon tuki

[!include [banner](../../includes/banner.md)]

Tässä ohjeaiheessa on tietoja verojen laskemisen ja kirjaamisen integroinnista siirtotilauksissa. Tämän toiminnon avulla voit määrittää verojen laskennan ja kirjauksen varastosiirtojen siirtotilauksissa. Euroopan unionin (EU) arvonlisäverosäädöksissä varastosiirtoja käsitellään yhteisön sisäisenä toimituksena ja yhteisön sisäisenä hankintana.

Tämän toiminnon konfiguroiminen ja käyttö edellyttää kolmen päävaiheen suoritusta:

1. **RCS:n määritys:** Määritä Regulatory Configuration Servicessa siirtotilausten verokoodin määrittämisen verotoiminto, verokoodit ja verokoodien kohdistettavuus.
2. **Financen asetukset:** Ota Microsoft Dynamics 365 Financessa käyttöön **Siirtotilauksen vero** -toiminto, määritä varaston veropalvelun parametrit ja määritä perusveroparametrit.
3. **Varastoasetukset:** Määritä siirtotilaustapahtumien varastokonfiguraatio.

## <a name="set-up-rcs-for-tax-and-transfer-order-transactions"></a>RCS:n määrittäminen veroa ja siirtotilaustapahtumia varten

Seuraavia ohjeita noudattamalla voit määrittää siirtotilauksen veron. Tässä olevassa esimerkissä siirtotilaus on Alankomaista Belgiaan.

1. Valitse **Verotoiminnot**-sivun **Versiot**-välilehdestä luonnosominaisuuden versio ja valitse sitten **Muokkaa**.

    ![Muokkauksen valitseminen.](../media/tax-feature-support-01.png)

2. Valitse **Verotoimintojen asetukset** -sivun **Verokoodit**-välilehdestä **Lisää** luodaksesi uusia verokoodeja. Tässä esimerkissä luodaan kolme verokoodia: **NL-Exempt**, **BE-RC-21** ja **BE-RC+21**.

    - Kun siirtotilaus lähetetään Alankomaiden varastosta, käytetään Alankomaiden ALV-vapautuskoodia  (**NL-Exempt**).
      
        Luo verokoodi **NL-Exempt**.
        1. Valitse **Lisää** ja kirjoita **Verokoodi**-kenttään **NL-Exempt**.
        2. Valitse **Verokomponentti**-kentässä **Nettosumman mukaan**.
        3. Valitse **Tallenna**.
        4. Valitse **Prosentti**-välilehdessä **Lisää**.
        5. Vaihda **On veroton** -arvoksi **Kyllä** **Yleiset**-osassa.

        ![NL-Exempt-verokoodi.](../media/tax-feature-support-02.png)

    - Kun siirtotilaus vastaanotetaan Belgian varastossa, käänteisen veloituksen menetelmää käytetään **BE-RC-21**- ja **BE-RC+21**-verokoodien avulla.
        
        Luo verokoodi **BE-RC-21**.      
        1. Valitse **Lisää** ja kirjoita **Verokoodi**-kenttään **BE-RC-21**.
        2. Valitse **Verokomponentti**-kentässä **Nettosumman mukaan**.
        3. Valitse **Tallenna**.
        4. Valitse **Prosentti**-välilehdessä **Lisää**.
        5. Kirjoita **Veroprosentti**-kenttään **-21**.
        6. Vaihda **On käänteinen veloitus** -arvoksi **Kyllä** **Yleiset**-osassa.
        7. Valitse **Tallenna**.

        ![BE-RC-21-verokoodi käänteiselle veloitukselle.](../media/tax-feature-support-03.png)
        
        Luo verokoodi **BE-RC+21**.
        1. Valitse **Lisää** ja kirjoita **Verokoodi**-kenttään **BE-RC-21**.
        2. Valitse **Verokomponentti**-kentässä **Nettosumman mukaan**.
        3. Valitse **Tallenna**.
        4. Valitse **Prosentti**-välilehdessä **Lisää**.
        5. Kirjoita **Veroprosentti**-kenttään **21**.
        6. Valitse **Tallenna**.

        ![BE-RC+21-verokoodi käänteiselle veloitukselle.](../media/tax-feature-support-04.png)

3. Määritä verokoodien kohdistettavuus.

    1. Valitse **Sarakkeiden hallinta** ja valitse sitten sarakkeet, joita käytetään käytettävyystaulun muodostamiseksi.

        > [!NOTE]
        > Varmista, että lisäät tauluun **Liiketoimintaprosessi**- ja **Veron suunta** -sarakkeet. Molemmat sarakkeet ovat olennaista siirtotilausten verojen toiminnallisuudessa.

    2. Lisää kohdistettavuusssäännöt. Älä jätä **Verokoodit**-, **Veroryhmä**- tai **Nimikkeen veroryhmä** -kenttiä tyhjiksi.
        
        Lisää uusi sääntö siirtotilauslähetykseen.
        1. Valitse **Soveltuvuussäännöt**-välilehdessä **Lisää**.
        2. Ota sääntö käyttöön siirtotilausta varten valitsemalla **Liiketoimintaprosessi**-kentässä **Varasto**.
        3. Kirjoita **Toimitus maasta/alueelta** -kenttään **NLD**.
        4. Kirjoita **Toimitus maahan/alueelle** -kenttään **BEL**.
        5. Valitse **Veron suunta**-kentässä **Tulos**, jos haluat, että sääntöä sovelletaan siirtotilauksen toimitukseen.
        6. Valitse **Verokoodit**-kentässä **NL-Exempt**.
        7. Syötä **Veroryhmä**- ja **Nimikkeen veroryhmä** -kentissä liittyvä arvonlisäveroryhmä ja nimikkeen arvonlisäveroryhmä, jotka on määritetty Finance-järjestelmässäsi.
        
        Lisää toinen sääntö siirtotilauksen vastaanottoon.
        1. Valitse **Soveltuvuussäännöt**-välilehdessä **Lisää**.
        2. Ota sääntö käyttöön siirtotilausta varten valitsemalla **Liiketoimintaprosessi**-kentässä **Varasto**.
        3. Kirjoita **Toimitus maasta/alueelta** -kenttään **NLD**.
        4. Kirjoita **Toimitus maahan/alueelle** -kenttään **BEL**.
        5. Valitse **Veron suunta**-kentässä **Syöte**, jos haluat, että sääntöä sovelletaan siirtotilauksen vastaanottoon.
        6. Valitse **Verokoodit**-kentästä **BE-RC+21** ja **BE-RC-21**.
        7. Syötä **Veroryhmä**- ja **Nimikkeen veroryhmä** -kentissä liittyvä arvonlisäveroryhmä ja nimikkeen arvonlisäveroryhmä, jotka on määritetty Finance-järjestelmässäsi.

        ![Soveltuvuussäännöt.](../media/image5.png)

4. Täydennä ja julkaise uusi vero-ominaisuusversio.

    [![Uuden version tilan muuttaminen.](../media/image6.png)](../media/image6.png)

## <a name="set-up-finance-for-transfer-order-transactions"></a>Financen määrittäminen siirtotilaustapahtumia varten

Ota käyttöön ja määritä verot siirtotilauksille seuraavien ohjeiden avulla.

1. Valitse Financessa **Työtilat** \> **Ominaisuuden hallinta**.
2. Etsi ja valitse luettelosta **Siirtotilauksen vero** -ominaisuus ja ota se sitten käyttöön valitsemalla **Ota käyttöön nyt**.

    > [!IMPORTANT]
    > **Siirtotilauksen vero** -ominaisuus on täysin riippuvainen veropalvelusta. Siksi se voidaan ottaa käyttöön vasta, kun olet asentanut veropalvelun.

    ![Siirtotilauksen vero -ominaisuus.](../media/image7.png)

3. Ota veropalvelu käyttöön ja valitse **Varasto**-liiketoimintaprosessi.

    > [!IMPORTANT]
    > Tämä vaihe on suoritettava jokaiselle Financen oikeushenkilölle, jossa haluat veropalvelun ja Siirtotilauksen vero -toiminnon olevan käytettävissä.

    1. Siirry kohtaan **Vero** \> **Asetukset** \> **Veromääritys** \> **Veropalvelun määritys**.
    2. Valitse **Liiketoimintaprosessi**-kentässä **Varasto**.

    ![Liiketoimintaprosessi-kentän määrittäminen.](../media/image8.png)

4. Varmista, että käänteinen veloitusmekanismi on määritetty. Siirry kohtaan **Kirjanpito** \> **Asetukset** \> **Parametrit** ja varmista sitten **Käänteinen veloitus** -välilehdessä, että **Ota käänteinen veloitus käyttöön** -asetuksen arvo on **Kyllä**.

    ![Ota käänteinen veloitus käyttöön -asetus.](../media/image9.png)

5. Varmista, että liittyvät verokoodit, veroryhmät, nimikkeen veroryhmät ja ALV-rekisterinumerot on määritetty Financessa veropalvelun ohjeistuksen mukaisesti.
6. Määritä väliaikainen siirtotili. Tämä vaihe on pakollinen vain, jos siirtotilaukseen sovellettavaa veroa ei sovelleta verovapautukseen tai käännetyn veloituksen verojen mekanismiin.

    1. Siirry kohtaan **Vero** \> **Asetukset** \> **Arvonlisävero** \> **Kirjanpidon kirjausryhmät**.
    2. Valitse **Väliaikainen siirto** -kentästä kirjanpitotili.

    ![Väliaikaisen siirtotilin valinta.](../media/image10.png)

## <a name="set-up-basic-inventory-for-transfer-order-transactions"></a>Perusvaraston määrittäminen siirtotilaustapahtumia varten

Näiden vaiheiden avulla voit määrittää perusvaraston, joka ottaa siirtotilaustapahtumat käyttöön.

1. Luo lähetys- ja vastaanottotoimipaikat eri maiden tai alueiden varastoille ja lisää kunkin toimipaikan ensisijainen osoite.

    1. Valitse **Varastonhallinta** \> **Asetukset** \> **Varasto** \> **Toimipaikat**.
    2. Valitse **Uusi**, jos haluat luoda toimipaikan, jonka liität varastoon myöhemmin.
    3. Toista vaihe 2 kaikille muille toimipaikoille, jotka sinun on luotava.

    > [!NOTE]
    > Yhden luodun toimipaikan nimi on oltava **Siirto**. Tämän menettelyn myöhemmässä vaiheessa tämä toimipaikka määritetään siirtovarastoon, jotta veroihin liittyvät varastotositteet voidaan kirjata siirtotilausten toimitus- ja vastaanottotapahtumiin. Siirtopaikan osoite ei ole merkityksellinen verolaskelman kannalta. Tämän vuoksi kenttä voidaan jättää tyhjäksi.

    ![Toimipaikkojen määritys.](../media/image11.png)

2. Luo lähetys-, siirto- ja vastaanottovarastot. Kaikki fyysisessä varastossa ylläpidettävät osoitetiedot ohittavat toimipaikan osoitteen veronlaskennan aikana.

    1. Valitse **Varastonhallinta** \> **Asetukset** \> **Varasto** \> **Varastot**.
    2. Valitse **Uusi**, jos haluat luoda fyysisien varaston ja liittää sen vastaavaan toimipaikkaan.
    3. Toista vaihe 2, jos haluat luoda fyysisen varaston kullekin toimipaikalle tarpeen mukaan.

    ![Fyysisten varastojen määrittäminen.](../media/image12.png)

    > [!NOTE]
    > Lähetysvarastolle siirtovarasto on valittava **Siirtovarasto**-kentässä siirtotilaustapahtumia varten.
    >
    > ![Siirtovaraston valitseminen.](../media/image13.png)

3. Varmista, että siirtotilaustapahtumien varastokirjauskonfiguraatio on määritetty.

    1. Siirry kohtaan **Varastonhallinta** \> **Määritys** \> **Kirjaus** \> **Kirjaus**.
    2. Varmista **Varasto**-välilehdessä, että kirjanpitotili on määritetty sekä **Varasto-otto**- että **Varastovastaanotto** -kirjausta varten.

        ![Varasto-oton ja varastovastaanoton kirjauksen määrittäminen.](../media/image14.png)

    3. Varmista, että kirjanpitotilille on määritetty **Yksiköiden väliset saatavat** -kirjaus.

        ![Yksiköiden väliset saatavat -kirjauksen määrittäminen.](../media/image15.png)

    4. Varmista, että kirjanpitotilille on määritetty **Yksiköiden väliset maksettavat** -kirjaus.

        ![Yksiköiden väliset maksettavat -kirjauksen määrittäminen.](../media/image16.png)
