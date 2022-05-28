---
title: Siirtotilausten verotoiminnon tuki
description: Tässä aiheessa kuvataan siirtotilausten uutta verotoimintoa veron laskentapalvelua käyttäen.
author: Kai-Cloud
ms.date: 10/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d95ea6795dc5777bfd37f8fbb3ebc47f2db337a0
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689211"
---
# <a name="tax-feature-support-for-transfer-orders"></a>Siirtotilausten verotoiminnon tuki

[!include [banner](../../includes/banner.md)]

Tässä ohjeaiheessa on tietoja verojen laskemisen ja kirjaamisen integroinnista siirtotilauksissa. Tämän toiminnon avulla voit määrittää verojen laskennan ja kirjauksen varastosiirtojen siirtotilauksissa. Euroopan unionin (EU) arvonlisäverosäädöksissä varastosiirtoja käsitellään yhteisön sisäisenä toimituksena ja yhteisön sisäisenä hankintana.

Tämän toiminnon konfiguroiminen ja käyttö edellyttää kolmen päävaiheen suoritusta:

1. **RCS:n määritys:** Määritä Regulatory Configuration Servicessa siirtotilausten verokoodin määrittämisen verotoiminto, verokoodit ja verokoodien kohdistettavuus.
2. **Dynamics 365 Financen määritys:** Ota Financessa käyttöön **Siirtotilauksen vero** -toiminto, määritä varaston veronlaskentapalvelun parametrit ja määritä perusveroparametrit.
3. **Varastoasetukset:** Määritä siirtotilaustapahtumien varastokonfiguraatio.

## <a name="set-up-rcs-for-tax-and-transfer-order-transactions"></a>RCS:n määrittäminen veroa ja siirtotilaustapahtumia varten

Seuraavia ohjeita noudattamalla voit määrittää siirtotilauksen veron. Tässä olevassa esimerkissä siirtotilaus on Alankomaista Belgiaan.

1. Valitse **Verotoiminnot**-sivun **Versiot**-välilehdestä luonnosominaisuuden versio ja valitse sitten **Muokkaa**.

2. Valitse **Verotoimintojen asetukset** -sivun **Verokoodit**-välilehdestä **Lisää** luodaksesi uusia verokoodeja. Tässä esimerkissä luodaan kolme verokoodia: **NL-Exempt**, **BE-RC-21** ja **BE-RC+21**.

    - Kun siirtotilaus lähetetään Alankomaiden varastosta, käytetään Alankomaiden ALV-vapautuskoodia  (**NL-Exempt**).
      
        Luo verokoodi **NL-Exempt**.
        1. Valitse **Lisää** ja kirjoita **Verokoodi**-kenttään **NL-Exempt**.
        2. Valitse **Verokomponentti**-kentässä **Nettosumman mukaan**.
        3. Valitse **Tallenna**.
        4. Valitse **Prosentti**-välilehdessä **Lisää**.
        5. Määritä **On veroton** -arvoksi **Kyllä** **Yleiset**-osassa.
        6. Syötä **Vapautuskoodi**-kenttään **EY**.

    - Kun siirtotilaus vastaanotetaan Belgian varastossa, käänteisen veloituksen menetelmää käytetään **BE-RC-21**- ja **BE-RC+21**-verokoodien avulla.
        
        Luo verokoodi **BE-RC-21**.      
        1. Valitse **Lisää** ja kirjoita **Verokoodi**-kenttään **BE-RC-21**.
        2. Valitse **Verokomponentti**-kentässä **Nettosumman mukaan**.
        3. Valitse **Tallenna**.
        4. Valitse **Prosentti**-välilehdessä **Lisää**.
        5. Kirjoita **Veroprosentti**-kenttään **-21**.
        6. Määritä **On käänteinen veloitus** -arvoksi **Kyllä** **Yleiset**-osassa.
        7. Valitse **Tallenna**.
        
        Luo verokoodi **BE-RC+21**.
        1. Valitse **Lisää** ja kirjoita **Verokoodi**-kenttään **BE-RC-21**.
        2. Valitse **Verokomponentti**-kentässä **Nettosumman mukaan**.
        3. Valitse **Tallenna**.
        4. Valitse **Prosentti**-välilehdessä **Lisää**.
        5. Kirjoita **Veroprosentti**-kenttään **21**.
        6. Valitse **Tallenna**.

3. Määritä veroryhmä.
    1. Valitse **Hallitse sarakkeita** ja valitse sitten rivikenttä **Veroryhmä**.
    2. Vallitse **->** ja sitten **OK**.
    3. Lisää veroryhmä valitsemalla **Lisää**.
    4. Syötä **Veroryhmä**-sarakkeeseen **AR-EU** ja valitse sitten verokoodi **NL-Exempt**.
    5. Lisää veroryhmä valitsemalla **Lisää**.
    6. Syötä **Veroryhmä**-sarakkeeseen **RC-VAT** ja valitse sitten verokoodit **BE-RC-21** ja **BE-RC+21**.
4. Määritä nimikkeen veroryhmä.
    1. Valitse **Hallitse sarakkeita** ja valitse sitten rivikenttä **Nimikkeen veroryhmä**.
    2. Vallitse **->** ja sitten **OK**.
    3. Lisää nimikkeen veroryhmä valitsemalla **Lisää**.
    4. Syötä **Nimikkeen veroryhmä** -kenttään **FULL**. Valitse verokoodit **BE-RC-21**, **BE-RC+21** ja **NL-Exempt**.
5. Määritä veroryhmän kohdistettavuus.

    1. Valitse **Sarakkeiden hallinta** ja valitse sitten sarakkeet, joita käytetään käytettävyystaulun muodostamiseksi.

        > [!NOTE]
        > Varmista, että lisäät tauluun **Liiketoimintaprosessi**- ja **Veron suunta** -sarakkeet. Molemmat sarakkeet ovat olennaista siirtotilausten verojen toiminnallisuudessa.

    2. Lisää kohdistettavuusssäännöt. Älä jätä **Veroryhmä**-kenttää tyhjäksi.
        
        Lisää uusi sääntö siirtotilauslähetykseen.
        1. Valitse **Soveltuvuussäännöt**-välilehdessä **Lisää**.
        2. Ota sääntö käyttöön siirtotilausta varten valitsemalla **Liiketoimintaprosessi**-kentässä **Varasto**.
        3. Kirjoita **Toimitus maasta/alueelta** -kenttään **NLD**.
        4. Kirjoita **Toimitus maahan/alueelle** -kenttään **BEL**.
        5. Valitse **Veron suunta**-kentässä **Tulos**, jos haluat, että sääntöä sovelletaan siirtotilauksen toimitukseen.
        6. Valitse **Veroryhmä**-kentässä **AR-EU**.
        
        Lisää toinen sääntö siirtotilauksen vastaanottoon.
        
        1. Valitse **Soveltuvuussäännöt**-välilehdessä **Lisää**.
        2. Ota sääntö käyttöön siirtotilausta varten valitsemalla **Liiketoimintaprosessi**-kentässä **Varasto**.
        3. Kirjoita **Toimitus maasta/alueelta** -kenttään **NLD**.
        4. Kirjoita **Toimitus maahan/alueelle** -kenttään **BEL**.
        5. Valitse **Veron suunta**-kentässä **Syöte**, jos haluat, että sääntöä sovelletaan siirtotilauksen vastaanottoon.
        6. Valitse **Veroryhmä**-kentässä **RC-VAT**.

6. Määritä nimikkeen veroryhmän kohdistettavuus.

    1. Valitse **Sarakkeiden hallinta** ja valitse sitten sarakkeet, joita käytetään käytettävyystaulun muodostamiseksi.
    2. Lisää kohdistettavuusssäännöt. Älä jätä **Nimikkeen veroryhmä**-kenttää tyhjäksi.
        
        Lisää uusi sääntö siirtotilauksen lähetykselle ja vastaanotolle.
        1. Valitse **Kohdistettavuussäännöt**-sivulla **Lisää**.
        2. Ota sääntö käyttöön siirtotilausta varten valitsemalla **Liiketoimintaprosessi**-kentässä **Varasto**.
        3. Valitse **Nimikkeen eroryhmä**-kentässä **FULL**.
7. Täydennä ja julkaise uusi vero-ominaisuusversio.


## <a name="set-up-finance-for-transfer-order-transactions"></a>Financen määrittäminen siirtotilaustapahtumia varten

Ota käyttöön ja määritä verot siirtotilauksille seuraavien ohjeiden avulla.

1. Valitse Financessa **Työtilat** > **Ominaisuuden hallinta**.
2. Etsi ja valitse luettelosta **Siirtotilauksen vero** -ominaisuus ja ota se sitten käyttöön valitsemalla **Ota käyttöön nyt**.

    > [!IMPORTANT]
    > **Siirtotilauksen vero** -ominaisuus on täysin riippuvainen veronlaskentapalvelusta. Siksi se voidaan ottaa käyttöön vasta, kun olet asentanut veronlaskentapalvelun.

    ![Siirtotilauksen vero -ominaisuus.](../media/image7.png)

3. Ota veronlaskentapalvelu käyttöön ja valitse **Varasto**-liiketoimintaprosessi.

    > [!IMPORTANT]
    > Tämä vaihe on suoritettava jokaiselle Financen oikeushenkilölle, jossa haluat veronlaskentapalvelun ja Siirtotilauksen vero -toiminnon olevan käytettävissä.

    1. Siirry kohtaan **Vero** > **Määritys** > **Veronmääritys** > **Veronlaskentaparametrit**.
    2. Valitse **Liiketoimintaprosessi**-kentässä **Varasto**.

4. Varmista, että käänteinen veloitusmekanismi on määritetty. Siirry kohtaan **Kirjanpito** \> **Asetukset** \> **Parametrit** ja varmista sitten **Käänteinen veloitus** -välilehdessä, että **Ota käänteinen veloitus käyttöön** -asetuksen arvo on **Kyllä**.

    ![Ota käänteinen veloitus käyttöön -asetus.](../media/image9.png)

5. Varmista, että liittyvät verokoodit, veroryhmät, nimikkeen veroryhmät ja ALV-rekisterinumerot on määritetty Financessa veronlaskentapalvelun ohjeistuksen mukaisesti.
6. Määritä väliaikainen siirtotili. Tämä vaihe on pakollinen vain, jos siirtotilaukseen sovellettavaa veroa ei sovelleta verovapautukseen tai käännetyn veloituksen verojen mekanismiin.

    1. Siirry kohtaan **Vero** > **Asetukset** > **Arvonlisävero** > **Kirjanpidon kirjausryhmät**.
    2. Valitse **Väliaikainen siirto** -kentästä kirjanpitotili.

       ![Väliaikaisen siirtotilin valinta.](../media/image10.png)

## <a name="set-up-basic-inventory-for-transfer-order-transactions"></a>Perusvaraston määrittäminen siirtotilaustapahtumia varten

Näiden vaiheiden avulla voit määrittää perusvaraston, joka ottaa siirtotilaustapahtumat käyttöön.

1. Luo lähetys- ja vastaanottotoimipaikat eri maiden tai alueiden varastoille ja lisää kunkin toimipaikan ensisijainen osoite.

    1. Valitse **Varastonhallinta** > **Asetukset** > **Varasto** > **Toimipaikat**.
    2. Valitse **Uusi**, jos haluat luoda toimipaikan, jonka liität varastoon myöhemmin.
    3. Toista vaihe 2 kaikille muille toimipaikoille, jotka sinun on luotava.

    > [!NOTE]
    > Yhden luodun toimipaikan nimi on oltava **Siirto**. Tämän menettelyn myöhemmässä vaiheessa tämä toimipaikka määritetään siirtovarastoon, jotta veroihin liittyvät varastotositteet voidaan kirjata siirtotilausten toimitus- ja vastaanottotapahtumiin. Siirtopaikan osoite ei ole merkityksellinen verolaskelman kannalta. Tämän vuoksi kenttä voidaan jättää tyhjäksi.

    ![Toimipaikkojen määritys.](../media/image11.png)

2. Luo lähetys-, siirto- ja vastaanottovarastot. Kaikki fyysisessä varastossa ylläpidettävät osoitetiedot ohittavat toimipaikan osoitteen veronlaskennan aikana.

    1. Siirry kohtaan **Varastonhallinta** > **Asetukset** > **Varasto** > **Varastot**.
    2. Valitse **Uusi**, jos haluat luoda fyysisien varaston ja liittää sen vastaavaan toimipaikkaan.
    3. Toista vaihe 2, jos haluat luoda fyysisen varaston kullekin toimipaikalle tarpeen mukaan.

       ![Fyysisten varastojen määrittäminen.](../media/image12.png)

    > [!NOTE]
    > Lähetysvarastolle siirtovarasto on valittava **Siirtovarasto**-kentässä siirtotilaustapahtumia varten.
    >
    > ![Siirtovaraston valitseminen.](../media/image13.png)

3. Varmista, että siirtotilaustapahtumien varastokirjauskonfiguraatio on määritetty.

    1. Siirry kohtaan **Varastonhallinta** > **Määritys** > **Kirjaus** > **Kirjaus**.
    2. Varmista **Varasto**-välilehdessä, että kirjanpitotili on määritetty sekä **Varasto-otto**- että **Varastovastaanotto** -kirjausta varten.

        ![Varasto-oton ja varastovastaanoton kirjauksen määrittäminen.](../media/image14.png)

    3. Varmista, että kirjanpitotilille on määritetty **Yksiköiden väliset saatavat** -kirjaus.

        ![Yksiköiden väliset saatavat -kirjauksen määrittäminen.](../media/image15.png)

    4. Varmista, että kirjanpitotilille on määritetty **Yksiköiden väliset maksettavat** -kirjaus.

        ![Yksiköiden väliset maksettavat -kirjauksen määrittäminen.](../media/image16.png)
        
        
  [!INCLUDE[footer-include](../../../includes/footer-banner.md)]
