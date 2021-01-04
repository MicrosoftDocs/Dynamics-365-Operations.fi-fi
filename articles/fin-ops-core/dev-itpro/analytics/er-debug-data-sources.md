---
title: Suoritettavan ER-muodon tietolähteiden vianmääritys tiedonkulun ja muunnoksen analysointia varten
description: Tässä ohjeaiheessa kerrotaan, miten voit korjata suoritetun ER-muodon tietolähteet ja ymmärtää paremmin konfiguroidun tietovuon ja muunnoksen.
author: NickSelin
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 3a486800f37dda7829aeeaa56a30285a92a61b9d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680779"
---
# <a name="debug-data-sources-of-an-executed-er-format-to-analyze-data-flow-and-transformation"></a>Suoritettavan ER-muodon tietolähteiden vianmääritys tiedonkulun ja muunnoksen analysointia varten

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

Kun [määrität](tasks/er-format-configuration-2016-11.md) sähköisen raportointi (ER) -ratkaisun tuottamaan lähteviä asiakirjoja, määrität menetelmät, joita käytetään tietojen noutamiseen sovelluksesta ja kirjoitetaan se luotavaan tuotokseen. Jotta ER-ratkaisun elinkaarituki olisi tehokkaampaa, ratkaisusi tulisi koostua ER-[tietomallista](general-electronic-reporting.md#DataModelComponent) ja sen [kartoitus](general-electronic-reporting.md#ModelMappingComponent)-komponenteista sekä ER-[formaatista](general-electronic-reporting.md#FormatComponentOutbound) ja sen kartoituskomponenteista, jotta mallikartoitus on sovelluskohtainen, kun taas muut komponentit ovat sovelluskohtaisia. Tämän vuoksi useat ER-komponentit saattavat [vaikuttaa](general-electronic-reporting.md#FormatComponentOutbound) tietojen syöttämisen yhteydessä luotuun tulostukseen.

Joskus luodun tuotoksen tiedot näyttävät erilaisilta kuin samat tiedot sovellustietokannassa. Tällöin haluat määrittää, mikä ER-komponentti on vastuussa tietojen muunnoksesta. ER-tietolähteen virheenkorjaustoiminto vähentää merkittävästi tähän tutkimukseen liittyvää aikaa ja kustannuksia. Voit keskeyttää ER-muodon suorittamisen ja avata tietolähteen virheenkorjausliittymän. Siellä voit selata käytettävissä olevia tietolähteitä ja valita yksittäisen tietolähteen suoritusta varten. Tämä manuaalinen suorittaminen simuloi tietolähteen suorittamista ER-muodon todellisen suorituksen aikana. Tulos esitetään sivulla, jolla voit analysoida vastaanotettuja tietoja.

Voit ottaa tietolähteen virheenkorjaustoiminnon käyttöön määrittämällä **Ota tietojen virheenkorjaus käyttöön muodon suorituksen yhteydessä** -vaihtoehdon Suorita vaihtoehdon arvoksi **Kyllä** ER-käyttäjäparametreissa. Tämän jälkeen voit käynnistää tietolähteen virheenkorjauksen, kun luot lähteviä asiakirjoja suorittamalla ER-muodon. **Aloita virheenkorjaus** -vaihtoehdon avulla voit myös aloittaa tietolähteen virheenkorjaustoiminnon, joka on konfiguroitu [ER-työvaiheen suunnittelutoiminnossa](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document).

Tässä ohjeaiheessa on ohjeita tietolähteen virheenkorjauksen käynnistämiseen suoritettavissa ER-muodoissa. Siinä selitetään, miten tiedot voivat auttaa tietovuon ja tietojen muunnosten ymmärtämiseksi. Tämän ohjeaiheen esimerkeissä käytetään toimittajamaksukäsittelyn liiketoimintaprosessia.

## <a name="limitations"></a>Rajoitukset

Tietolähteen virheenkorjauksen avulla voidaan käyttää sellaisten tietolähteiden tietoja, joita käytetään lähtevien tiedostojen luomisessa suoritettaville eri muodoissa. Sitä ei voi käyttää sellaisten ER-muotojen tietolähteiden vian korjaukseen, jotka on suunniteltu jäsentämään saapuvia tiedostoja.

Seuraavat ER-muotojen asetukset eivät ole käytettävissä tietolähteen virheen korjausta varten:

- Lomakkeen muunnokset
- Oikeellisuustarkistussääntöjen muotoileminen ja määrittäminen
- Lausekkeiden ottaminen käyttöön
- Muistissa olevan tiedonkeräyksen tiedot

## <a name="prerequisites"></a>Edellytykset

- Tässä ohjeaiheessa olevien esimerkkien suorittaminen edellyttää käyttöoikeutta johonkin seuraavaan [rooliin](../sysadmin/tasks/assign-users-security-roles.md):

    - Sähköisen raportoinnin kehittäjä
    - Sähköisen raportoinnin toiminnallinen konsultti
    - Järjestelmänvalvoja

- Yritykselle on asetettava **DEMF**.

- Tämän ohjeaiheen [lisäyksen 1](#appendix1) vaiheiden mukaisesti voit ladata toimittajien maksuissa tarvittavien Microsoft er-ratkaisujen komponentit.
- Tämän ohjeaiheen [Lisäyksessä 2](#appendix2) olevien ohjeiden avulla voit valmistella ostoreskontran toimittajamaksun käsittelyä varten käyttämällä ER-ratkaisua, jonka voit ladata.

## <a name="process-a-vendor-payment-to-get-a-payment-file"></a>Toimittajamaksun käsitteleminen siten, että se saa maksutiedoston

1. Käsittele toimittajamaksuja tämän ohjeaiheen [Lisäyksen 3](#appendix3) ohjeiden mukaisesti.

    ![Toimittajamaksujen käsittely käynnissä](./media/er-data-debugger-process-payment.png)

2. Lataa ja tallenna zip-tiedosto paikalliseen tietokoneeseen.
3. Pura **ISO20022 Credit transfer.xml**-maksutiedosto zip-tiedostosta.
4. Avaa purettu maksutiedosto XML-tiedoston katseluohjelman avulla.

    Toimittajan pankkitilin kansainvälinen pankkitilin numero (IBAN)-koodi ei sisällä välilyöntejä maksutiedostossa. Siksi se eroaa **pankkitilit**-sivulla [syötetystä](#enteredIBANcode) arvosta.

    ![IBAN-koodi ilman välilyöntejä](./media/er-data-debugger-payment-file.png)

    Voit käyttää ER-tietolähteen virheenkorjaustoimintoa, kun haluat tietää, mitä ER-ratkaisun osaa käytetään IBAN-koodin välien lyhentämiseen.

## <a name="turn-on-data-source-debugging"></a>Tietolähteen virheenkorjauksen ottaminen käyttöön

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Valitse **Määritykset**-sivun toimintoruudun **Määritykset**-välilehden **Lisämääritykset**-ryhmässä **Käyttäjäparametrit**.
3. Määritä **Ota tietojen virheenkorjaus käyttöön muodon suorituksen yhteydessä** -asetuksen arvoksi **Kyllä**.

    > [!NOTE]
    > Tämä parametri on käyttäjä- ja yrityskohtainen.

    ![Käyttäjän parametrit -valintaikkuna](./media/er-data-debugger-user-parameters.png)

## <a name="process-a-vendor-payment-for-debugging"></a>Toimittajan summan käsitteleminen virheen korjausta varten

1. Käsittele toimittajamaksuja tämän ohjeaiheen [Lisäyksen 3](#appendix3) ohjeiden mukaisesti.
2. Vahvista, että haluat keskeyttää toimittajan maksujenkäsittelyn ja käynnistää sen sijaan tietolähteen **virheenkorjauksen tietolähteet** -sivulla, valitsemalla sanomaruudun vaihtoehdon **Kyllä**.

    ![Vahvistussanomaruutu](./media/er-data-debugger-start-debugging.png)

## <a name="debug-data-sources-that-are-used-in-payment-processing"></a>Virheenkorjauksen tietolähteet, joita käytetään maksukäsittelyssä

### <a name="debug-the-model-mapping"></a>Mallimäärityksen virheenkorjaus

1. Valitse **Tietolähteiden virheenkorjaus** -sivun toimintoruudussa **Mallimääritys**, jonka avulla voit aloittaa virheenkorjauksen tästä ER-komponentista.
2. Valitse vasemmanpuoleisen tietolähderuudun **\$notSentTransactions**-tietolähde ja valitse sitten **Lue kaikki tiedot**.

    Voit valita **Lue 1 tietue**, **lue 10 tietuetta**, **lue 100 tietuetta** tai **lue kaikki tietueet** pakottamaan valitun tietolähteen lukemiseen tarvittavan määrän tietueita. Näin voit simuloida tietolähteen käyttöä käynnissä olevan ER-muodon avulla.

3. Valitse oikealla olevassa tietoruudussa **Laajenna kaikki**.

    Voit nähdä, että **tietueluettelo**-tyypin valittu tietolähde sisältää yhden tietueen.

4. Laajenna **\$notSentTransactions**-tietolähde ja valitse sisäkkäinen **vendBankAccountInTransactionCompany()**-menetelmä.
5. Laajenna **vendBankAccountInTransactionCompany()**-menetelmä ja valitse sisäkkäinen **IBAN**-kenttä.
6. Valitse **Hae arvo**.

    Valitsemalla **Hae arvo** voit pakottaa valitun tietolähteen valitun kentän arvon luettavaksi. Näin voit simuloida tämän kentän käyttöä käynnissä olevan ER-muodon avulla.

7. Valitse **Laajenna kaikki**.

    ![Mallimäärityksen IBAN-kentän arvo](./media/er-data-debugger-debugging-model-mapping.png)

    Kuten näette, mallikartoitus ei ole vastuussa katkenneista välilyönneistä, sillä toimittajan pankkitilin palauttama IBAN-koodi sisältää välilyöntejä. Tämän vuoksi tietolähteen virheenkorjausta on jatkettava.

### <a name="debug-the-format-mapping"></a>Muodon yhdistämismäärityksen virheenkorjaus

1. Valitse **Tietolähteiden virheenkorjaus** -sivun toimintoruudussa **Muodon määritys**, jonka avulla voit jatkaa virheenkorjauksen tästä ER-komponentista.
2. Valitse **\$PaymentByDebtor**-tietolähde ja valitse sitten **Lue kaikki tietueet**.
3. Laajenna **\$PaymentByDebtor**.
4. Laajenna **\$PaymentByDebtor.Lines** ja valitse sitten **Lue kaikki tietueet**.
5. Laajenna **\$PaymentByDebtor.Lines.CreditorAccount**.
6. Laajenna **\$PaymentByDebtor.Lines.CreditorAccount.Identification** ja valitse sitten **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN**.
7. Valitse **Hae arvo**.
8. Valitse **Laajenna kaikki**.

    ![Muodon määrityksen IBAN-kentän arvo](./media/er-data-debugger-debugging-format-mapping.png)

    Kuten näette, mallikartoituksen tietolähteet eivät ole vastuussa katkenneista välilyönneistä, sillä toimittajan pankkitilin palauttama IBAN-koodi sisältää välilyöntejä. Tämän vuoksi tietolähteen virheenkorjausta on jatkettava.

### <a name="debug-the-format"></a>Muodon virheenkorjaus

1. Valitse **Tietolähteiden virheenkorjaus** -sivun toimintoruudussa **Muoto**, jonka avulla voit jatkaa virheenkorjauksen tästä ER-komponentista.
2. Laajenna muotoiluelementit ja valitse **ISO20022CTReports** \> **XMLHeader** \> **Tiedosto** \> **CstmrCdtTrfInitn** \> **PmtInf** ja valitse sitten **Lue kaikki tietueet**.
3. Laajenna muotoiluelementit ja valitse **ISO20022CTReports** \> **XMLHeader** \> **Tiedosto** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** ja valitse sitten **Lue kaikki tietueet**.
4. Laajenna muotoiluelementit ja valitse **ISO20022CTReports** \> **XMLHeader** \> **Tiedosto** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Tunnus** \> **IBAN** \> **BankIBAN** ja valitse sitten **Hae arvo**.
5. Valitse **Laajenna kaikki**.

    ![Muodon IBAN-kentän arvo](./media/er-data-debugger-debugging-format.png)

   Kuten näette, muodon sidonta ei ole vastuussa katkenneista välilyönneistä, sillä toimittajan pankkitilin palauttama IBAN-koodi sisältää välilyöntejä. Siksi **BankIBAN**-elementti on konfiguroitu käyttämään muodon muutosta, joka katkaisee välit.

6. Sulje tietolähteen virheenkorjaus.

### <a name="review-the-format-transformations"></a>Tarkastele muodon muunnoksia

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Valitse **Konfiguraatiot**-sivulla **maksumalli** \> **ISO20022-tilisiirto**.
3. Valitse **Suunnitteluohjelma** ja laajenna sitten elementit valitaksesi **Tedosto** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Tunnus** \> **IBAN** \> **BankIBAN**.

    ![BankIBAN-elementti Muodon suunnittelija -sivulla](./media/er-data-debugger-referred-transformation.png)

    Kuten näette, **BankIBAN**-elementti on määritetty käyttämään **poista ei aakkosnumeerisia** -muunnosta.

4. Valitse **Muunnokset**-välilehti.

    ![BankIBAN-elementin muunnokset -välilehti](./media/er-data-debugger-transformation.png)

    Kuten näette, **Poista ei-aakkosnumeerinen** -muunnos on määritetty käyttämään lauseketta, joka katkaisee välit annetun tekstimerkkijonon väliltä.

## <a name="start-to-debug-in-the-operation-designer"></a>Aloita virheenkorjaus toiminnon suunnittelussa

Kun määrität ER-muodon luonnosversion, joka voidaan suorittaa suoraan toiminnon suunnittelutoiminnosta, voit käyttää tietolähteen virheenkorjausta valitsemalla toimintoruudusta **Aloita virheenkorjaus**.

![Muotoilun suunnittelu -sivun virheenkorjauspainikkeen käynnistäminen](./media/er-data-debugger-run-from-designer.png)

Muokattavan ER-muodon määritys- ja muotoilukomponentit ovat käytettävissä virheenkorjausta varten.

## <a name="start-to-debug-in-the-model-mapping-designer"></a>Aloita virheenkorjaus mallin määrityksen suunnittelussa

Kun määrität ER-muodon määrityksen, joka voidaan suorittaa **Muodon määritys**-sivulta, voit käyttää tietolähteen virheenkorjausta valitsemalla toimintoruudusta **Aloita virheenkorjaus**.

![Mallin määrityksen suunnittelu -sivun virheenkorjauspainikkeen käynnistäminen](./media/er-data-debugger-run-from-designer-mapping.png)

Muokattavan ER-määrityksen mallimäärityskomponentti on käytettävissä virheen korjausta varten.

## <a name="appendix-1-get-an-er-solution"></a><a name="appendix1"></a>Lisäys 1: ER-ratkaisun hankkiminen

### <a name="download-an-er-solution"></a>Lataa ER-ratkaisu

Jos haluat käyttää ER-ratkaisua sähköisen maksutiedoston luomiseen käsiteltävälle toimittajamaksulle, voit [ladata](download-electronic-reporting-configuration-lcs.md) **ISO20022-tilisiirron** ER-maksumuotoa, joka on käytettävissä Microsoft Dynamics Lifecycle Servicesin (LCS) jaetun käyttöomaisuuden kirjastossa tai yleisestä tietovarastosta.

![ER-maksumuodon tuominen konfiguraation tietovarasto -sivulla](./media/er-data-debugger-import-from-repo.png)

Valitun ER-muodon lisäksi seuraavat [kokoonpanot](general-electronic-reporting.md#Configuration) on tuotava automaattisesti Microsoft Dynamics 365 Finance -instanssiin osana **ISO20022-tilisiirron** ER-ratkaisua:

- **Maksun malli** [ER-tietomallien määritys](general-electronic-reporting.md#DataModelComponent)
- **ISO20022-tilisiirto** [ER-muodon konfiguraatio](general-electronic-reporting.md#FormatComponentOutbound)
- **Maksumallin yhdistämismääritys 1611** [ER-mallin yhdistämismääritys](general-electronic-reporting.md#ModelMappingComponent)
- **Maksumallin yhdistämismääritys kohteeseen ISO20022** ER-mallin yhdistämismääritys

Nämä konfiguraatiot löytyvät ER-kehyksen **Konfiguroinnit**-sivulta (**Organisaation hallinta** \> **Sähköinen raportointi** \> **Kokoonpanot**).

![Tuodut määritykset määrityssivulla](./media/er-data-debugger-configurations.png)

Jos jokin aiemmin luetelluista konfiguraatioista puuttuu määrityspuusta, ne on ladattava manuaalisesti LCS-jaetun käyttöomaisuuden kirjastosta samalla tavalla kuin **ISO20022-tilisiirron** ER-maksumuoto on ladattu.

### <a name="analyze-the-downloaded-er-solution"></a>Ladatun ER-ratkaisun analysoiminen

#### <a name="review-the-model-mapping"></a>Mallin määrityksen tarkastelu

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Valitse **Maksumalli** \> **Maksumallin kartoitus 1611**.
3. Valitse **Suunnittelu**.
4. Valitse **Maksumallin yhdistämismääritys ISO20022** -kartoitustietue.
5. Valitse **Suunnittelu** ja tarkista sitten avattava mallimääritys.

    Huomaa, että tietomallin **Maksut**-kenttä on sidottu **\$notSentTransactions**-tietolähteeseen, joka palauttaa käsiteltävien toimittajien maksurivien luettelon.

    ![Mallikartoituksen suunnittelusivun maksukenttä](./media/er-data-debugger-model-mapping.png)

#### <a name="review-the-format-mapping"></a>Muodon määrityksen tarkastelu

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Valitse **Maksumalli** \> **ISO20022-tilisiirto**.
3. Valitse **Suunnittelu**.
4. Tarkista **Yhdistämismääritys**-välilehdestä avattava muotomääritys.

    Huomaa, että **Asiakirja** \> **ICstmrCdtTrfInitn** \> **PmtInf**-elementti kohdassa **ISO20022CTReports** \> **XMLHeader**-tiedosto on sidottu **\$PaymentByDebtor**-tietolähteeseen, joka on määritetty tietomallin **Maksu**-kentän tietueiden ryhmittelemiseen.

    ![PmtInf-elementti Muodon suunnittelija -sivulla](./media/er-data-debugger-format-mapping.png)

#### <a name="review-the-format"></a>Muodon tarkastelu

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Valitse **Maksumalli** \> **ISO20022-tilisiirto**.
3. Valitse **Suunnittelu** ja tarkista sitten avattava muoto.

    Huomaa, että **Tiedosto** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Tunnus** \> **IBAN** \> **BankIBAN** on määritetty antamaan toimittajatilin IBAN-koodi maksutiedostossa.

    ![BankIBAN-elementti Muodon suunnittelija -sivulla](./media/er-data-debugger-format.png)

## <a name="appendix-2-configure-accounts-payable"></a><a name="appendix2"></a>Liite 2: Ostoreskontran määrittäminen

### <a name="modify-a-vendor-property"></a>Toimittajan ominaisuuden muokkaaminen

1. Siirry kohtaan **Ostoreskontra** \> **Toimittajat** \> **Kaikki toimittajat**.
2. Valitse toimittaja **DE-01002** ja valitse sitten **Toimittaja**-välilehden **Määritä**-ryhmässä **Pankkitilit**.
3. Kirjoita **Tunnus**-pikavälilehden **IBAN**-kenttään <a name="enteredIBANcode"></a> **GB33 BUKB 2020 1555 5555 55**.
4. Valitse **Tallenna**.

![IBAN-kenttä määritetty toimittajan pankkitilit -sivulla](./media/er-data-debugger-iban.png)

### <a name="set-up-a-method-of-payment"></a>Määritä maksutapa

1. Valitse **Ostoreskontra** \> **Maksun asetukset** \> **Maksutavat**.
2. Valitse **SEPA CT**-maksutapa.
3. Määritä **Tiedostomuodot**-pikavälilehden **Tiedostomuodot**-osassa **Yleinen sähköinen vientimuoto** -kohdan asetukseksi **Kyllä**.
4. Valitse **Vientimuodon konfigurointi** -kentässä **ISO20022-tilisiirto**-ER-muoto.
5. Valitse **Tallenna**.

![Tiedostomuodon asetukset toimitustapasivulla](./media/er-data-debugger-payment-method.png)

### <a name="add-a-vendor-payment"></a>Lisää toimittajamaksu

1. Valitse **Ostoreskontra** \> **Maksut** \> **Toimittajan maksukirjauskansio**.
2. Lisää uusi maksukirjauskansio.
3. Valitse **Rivit** ja lisää uusi toimitusrivi.
4. Valitse **Tili**-kentässä toimittaja **DE-01002**.
5. Syötä **Debet**-kenttään arvo.
6. Valitse **Maksutapa**-kentässä **SEPA CT**.
7. Valitse **Tallenna**.

![Toimittajamaksun lisäys toimittajan maksut -sivulla](./media/er-data-debugger-payment-journal.png)

## <a name="appendix-3-process-a-vendor-payment"></a><a name="appendix3"></a>Liite 3: Toimittajamaksun käsittely

1. Valitse **Ostoreskontra** \> **Maksut** \> **Toimittajan maksukirjauskansio**.
2. Valitse **Toimittajan maksukirjauskansio** -sivulla aiemmin luomasi kirjauskansio ja valitse sitten **Rivit**.
3. Valitse ensin maksurivi ja sitten **Maksun tila** \> **Ei mitään**.
4. Valitse **Muodosta maksut**.
5. Valitse **Maksutapa**-kentässä **SEPA CT**.
6. Valitse **Pankkitili**-kentässä **DEMF OPER**.
7. Valitse **Luo maksuja** -valintaikkunassa **OK**.
8. Valitse **Sähköisen raportin parametrit** -valintaikkunasta **OK**.
