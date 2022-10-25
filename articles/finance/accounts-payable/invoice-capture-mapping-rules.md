---
title: Invoice Capture -ratkaisun vastaavuusmäärityksen säännöt
description: Tässä artikkelissa on tietoja Invoice Capture -ratkaisun vastaavuusmääritysten sääntöjen asetuksesta.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: cd0d06f7fd3ed946756e975d0706687c2d4acc93
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691177"
---
# <a name="invoice-capture-solution-mapping-rules"></a>Invoice Capture -ratkaisun vastaavuusmäärityksen säännöt

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Vastaavuusmäärityksen säännöt tuovat peruspäätiedot Microsoft Dynamics 365 Financesta tai toiminnanohjausjärjestelmästä (ERP). Kun vastaavuusmäärityksen säännöt on määritetty, johdetaan toimittajan laskujen luomiseksi Financessa vaaditut tiedot. Kun käytetään vastaavuusmäärityksen sääntöjä, ostoreskontran käsittelijä tarkistaa tilan sen sijaan, että kaikki kenttien puuttuvat arvot tulisi täyttää manuaalisesti.

Vastaavuusmäärityksen sääntöjä on seuraavat neljä eri tyyppiä:

- Yritys
- Toimittajanro
- Nimike
- Kulutyyppi

## <a name="manage-mapping-rules-by-using-the-app"></a>Vastaavuusmäärityksen sääntöjen hallinta sovelluksen avulla

Voit hallita vastaavuusmäärityksen sääntöjä sovelluksen avulla valitsemalla **Asetukset**. **Vastaavuusmäärityksen säännön asetukset** -välilehdessä on seuraavat neljä vaihtoehtoa:

- Yritys 
- Toimittajanro 
- Nimikkeen vastaavuusmääritys 
- Kulutyyppi

Voit valita esimerkiksi **Yhdistyksen vastaavuusmäärityksen säännöt** -vaihtoehdon. Yrityksen koodi tunnistetaan käyttämällä yrityksen nimeä, osoitetta ja verorekisteröintinumeroa. Jos säännön nimi on **LE-USPM** ja yrityksen nimessä on Contoso Robotics USA -teksti, yrityksen koodi on **USPM**.

Sivulla näkyvät kaikki aktiiviset vastaavuusmäärityksen säännöt. Jos haluat tarkastella passiivia vastaavuusmäärityksen sääntöjä, valitse **Aktiiviset yrityksen vastaavuusmäärityksen säännöt** ja valitse sitten **Passiiviset yrityksen vastaavuusmäärityksen säännöt**.

Vastaavuusmäärityksen säännöissä ovat käytettävissä alla olevat toiminnot.

### <a name="create-a-mapping-rule"></a>Vastaavuusmäärityksen säännön luominen

Vastaavuusmäärityksen säännön voi luoda kahdella seuraavalla tavalla:

- Luo uusi vastaavuusmäärityksen sääntö valitsemalla **Uusi**. Lisää sitten vastaavuusmäärityksen säännön tiedot. **Säännön nimen** arvon on oltava yksilöivä kaikissa vastaavuusmäärityksen säännön tyypeissä.
- Jos valitset aiemmin luodun vastaavuusmäärityksen säännön, **Kopioi**-painike on käytettävissä. Valitse se ja valitse sitten avautuvassa valintaikkunassa **OK**. Vastaavuusmäärityksen sääntö luodaan kopioimalla valittu sääntö.

### <a name="edit-a-mapping-rule"></a>Vastaavuusmäärityksen säännön muokkaaminen

Jos haluat muokata vastaavuusmäärityksen sääntöä, valitse kenttä ja muuta arvoa.

### <a name="activatedeactivate-mapping-rules"></a>Vastaavuusmäärityksen sääntöjen aktivoiminen ja aktivoinnin poistaminen

Jos haluat poistaa vähintään yhden vastaavuusmäärityksen säännön aktivoinnin, valitse se **Aktiiviset vastaavuusmäärityksen säännöt** -sivulla ja valitse sitten **Poista aktivointi**. Säännöt siirretään **Aktiiviset vastaavuusmäärityksen säännöt** -sivulta **Passiiviset vastaavuusmäärityksen säännöt** -sivulle.

Samoin jos haluat aktivoida vähintään yhden vastaavuusmäärityksen säännön, valitse se **Passiiviset vastaavuusmäärityksen säännöt** -sivulla ja valitse sitten **Aktivoi**.

### <a name="remove-mapping-rules"></a>Vastaavuusmäärityksen sääntöjen poistaminen

Jos haluat poistaa vastaavuusmäärityksen sääntöjä, valitse ne ja valitse sitten **Poista**.

### <a name="check-for-conflicts"></a>Ristiriitojen tarkistaminen

Jos kahdella vastaavuusmäärityksen säännöllä on samat **yrityksen** ja **toimittajatilin** arvot, mutta erilaiset **nimikkeen nimen** arvot, havaitaan ristiriita, eikä vastaavuusmäärityksen sääntöä luoda tai päivitetä.

## <a name="importexport-mapping-rules-from-excel"></a>Vastaavuusmäärityksen sääntöjen tuominen/vieminen Excelistä

Excel-apuohjelmaa voi käyttää erän sääntöjen hallinnassa. Käytettävissä ovat seuraavat asetukset:

- Lataa Excel-malli.
- Vie Exceliin.
- Tuo Excelistä.

### <a name="download-an-excel-template"></a>Excel-mallin lataaminen

Jos haluat ladata Excel-mallin, valitse **Lataa malli**. Valitse sitten malliin sisällytettävät kentät.

### <a name="export-to-excel"></a>Vie Exceliin

Voit viedä tietoja kahdella seuraavalla tavalla:

- Avaa tiedosto Excelissä valitsemalla **Avaa Excel Onlinessa**. Voit sitten muokata tiedostoa online-tilassa. Kun olet valmis, valitse **Tallenna**. Kaikki muutokset tallennetaan **Vastaavuusmäärityksen sääntö** -sivulle.
- Valitse **Lataa laskentataulukko**, jos haluat ladata vastaavuusmäärityksen säännöt sisältävän Excel-tiedoston. Voit sitten muokata tiedostoa. Kun olet valmis, lataa päivitetty laskentataulukko valitsemalla **Tuo Excelistä**.

### <a name="import-from-excel"></a>Tuo Excelistä

1. Tuo tiedot XLSX-tiedostosta valitsemalla **Tuo Excelistä**. Voit tuoda myös CSV- ja XML-tiedostoja. Päätä ennen tuontia, sallitaanko kaksoiskappaleet.
2. Valitse **Tarkista vastaavuusmääritys**, jos haluat tarkistaa määritteiden vastaavuusmäärityksen ja määrittää, ovatko ne oikein. Vastaavuusmäärityksen suhdetta voi muokata.
3. Kun kaikki on tehty, aloita tuonti valitsemalla **Tee tuonti valmiiksi**.
4. Voit valita **Seuraa prosessia**, jos haluat seurata tuontiprosessin edistymistä.

    Tuonnin tila päivitetään **Lopeta**-tilasta **Jäsennetään**-tilaksi, sitten **Muunnetaan** ja lopuksi **Valmis**.

Kun tuontiprosessi on valmis, näytetään onnistumisten, osittaisten epäonnistumisten, virheiden ja käsiteltyjen kohteiden kokonaismäärä.
