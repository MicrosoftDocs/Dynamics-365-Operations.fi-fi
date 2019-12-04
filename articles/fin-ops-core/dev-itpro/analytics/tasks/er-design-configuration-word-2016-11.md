---
title: Suunnittele ER-konfiguraatiot voidaksesi luoda raportteja Word-muodossa
description: Seuraavissa vaiheissa selitetään, miten käyttäjä, jolla on järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli, voi määrittää sähköisen raportoinnin muotoja luomaan raportteja Microsoft Word -tiedostoina.
author: NickSelin
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 327f03435ab55551953fd998dd89c831c76c4c26
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182597"
---
# <a name="design-er-configurations-to-generate-reports-in-word-format"></a>Suunnittele ER-konfiguraatiot voidaksesi luoda raportteja Word-muodossa

[!include [task guide banner](../../includes/task-guide-banner.md)]

Seuraavissa vaiheissa selitetään, miten käyttäjä, jolla on järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli, voi määrittää sähköisen raportoinnin (ER) muotoja luomaan raportteja Microsoft Word -tiedostoina. Nämä vaiheet voidaan suorittaa GBSI-yrityksessä.

Näiden vaiheiden suorittaminen edellyttää, että ER-määrityksen luonti OPENXML-muotoisten raporttien luomiseksi -tehtäväoppaan vaiheet on suoritettu ensin. Lisäksi malliraporttia varten on etukäteen ladattava ja tallennettava paikallisesti seuraavat mallit:

- [Maksuraportin malli](https://go.microsoft.com/fwlink/?linkid=862266)
- [Maksuraportin sidottu malli](https://go.microsoft.com/fwlink/?linkid=862266)


Nämä ohjeet koskevat toimintoa, joka lisättiin Microsoft Dynamics 365 for Operations -versiossa 1611.


## <a name="select-the-existing-er-report-configuration"></a>Aiemmin luodun ER-raporttimäärityksen valitseminen
1. Siirry kohtaan **siirtymisruutu > Moduulit > organisaation hallinto > Työtilat > Sähköinen raportointi**. Varmista, että konfiguraation lähde, Litware Inc., on valittu aktiiviseksi.  
2. Valitse **Raportointikonfiguraatiot**. Käytämme aiemmin luotuja ER-määrityksiä, jotka on alun perin suunniteltu luomaan raportti OPENXML-muodossa.  
3. Laajenna puussa solmu Payment model.
4. Valitse puusta Maksumalli\Laskentataulukkoraportin esimerkki.
5. Valitse Suunnittelutoiminto.

## <a name="replace-the-excel-template-with-the-word-template"></a>Excel-malliin korvaaminen Word-mallilla

Tällä hetkellä OPENXML-muotoisen raportin luonnissa käytetään mallina Excel-tiedostoa. Raporttimalli tuodaan Word-muodossa.

1. Napsauta **Liitteet**. Korvaa aiemmin luotu Excel-malli aiemmin ladatulla Word-mallilla SampleVendPaymDocReport.docx. Huomaa, että tässä mallissa on vain ER-raporttina luotavan asiakirjan asettelu.  
2. Valitse **Poista**.
3. Valitse **Kyllä**.
4. Valitse **Uusi**.
5. Napsauta **Tiedosto**.
6. Valitse **Selaa**. Siirry aiemmin ladattuun asiakirjaan SampleVendPaymDocReport.docx ja valitse se. Valitse **OK**. Valitse edellisessä vaiheessa lataamasi malli.  
7. Syötä tai valitse **Malli**-kentän arvo.

## <a name="extend-the-word-template-by-adding-a-custom-xml-part"></a>Word-mallin laajentaminen lisäämällä mukautettu XML-osa
1. Valitse **Tallenna**. Määritysmuutosten tallennuksen lisäksi tallennustoiminto myös päivittää liitteenä olevan Word-mallin. Suunnittelun muodon rakenne siirretään liitettyyn Word-asiakirjaan uutena mukautettuna, Raportti-nimisenä XML-osana. Huomaa, että ER-raporttina luotavan asiakirjan asettelun lisäksi liitetty Word-malli sisältää myös tietorakenteen, jonka tiedot ER täyttää malliin suorituksen aikana.  
2. Napsauta **Liitteet**.
    + Mukautetun Raportti-XML-osan elementit on nyt sidottava Word-asiakirjan osiin.  
    + Jos olet käyttänyt Word-asiakirjoja, jotka on suunniteltu mukautettujen XML-osien elementteihin sidottuja sisällön ohjausobjekteja sisältäviksi lomakkeiksi, luo kyseinen asiakirja toistamalla kaikki seuraavan alitehtävän vaiheet. Lisätietoja on kohdassa [Luo lomakkeita, jotka käyttäjät täyttävät tai tulostavat Wordissa](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US). Muussa tapauksessa voit ohittaa kaikki seuraavan alitehtävän vaiheet.  

## <a name="get-word-with-custom-xml-part-to-do-data-bindings"></a>Mukautetun XML-osan sisältävän Word-asiakirjan hakeminen tietojen sidontaa varten

Avaa tämän asiakirja Wordissa ja toimi seuraavasti:  
1. Avaa Word-kehittäjät-välilehti (muokkaa valintanauhaa, jos se ei ole vielä käytettävissä.)
2. Valitse XML-määritys -ruutu.
3. Valitse mukautettu Raportti-XML-osa valintaruudussa.
4. Yhdistä valitun mukautetun XML-osan elementtien ja Word-asiakirjan sisällön ohjausobjektien määritykset.  5. Tallenna päivitetty Word-asiakirja paikalliseen asemaan.  

## <a name="upload-the-word-template-with-custom-xml-part-bounded-to-content-controls"></a>Sisällön ohjausobjekteihin sidottuja mukautettuja XML-osia sisältävän Word-mallin lataaminen palvelimeen
1. Valitse **Poista**.
2. Valitse **Kyllä**. Lisää uusi malli. Jos olet suorittanut edellisen vaiheen alitehtävät, valitse valmisteltu ja paikallisesti tallennettu Word-asiakirja. Valitse muussa tapauksessa aiemmin ladattu MS Word -malli SampleVendPaymDocReportBounded.docx.  
3. Valitse **Uusi**.
4. Napsauta **Tiedosto**.
5. Valitse **Selaa**. Siirry aiemmin ladattuun asiakirjaan SampleVendPaymDocReportBounded.docx ja valitse se. Valitse **OK**.
6. Valitse **Malli**-kentässä edellisessä vaiheessa lataamasi asiakirja.
7. Valitse **Tallenna**.
8. Sulje sivu.

## <a name="execute-the-format-to-create-word-output"></a>Word-asiakirjan luovan muodon suorittaminen
1. Valitse **toimintoruudussa** **Konfiguroinnit**.
2. Valitse **Käyttäjän parametrit**.
3. Valitse **Suorita asetukset** -kentässä Kyllä.
4. Valitse **OK**.
5. Valitse **Muokkaa**.
6. Valitse **Suorita luonnos** -kentässä Kyllä.
7. Valitse **Tallenna**.
8. Sulje sivu.
9. Sulje sivu.
10. Siirry **siirtymisruudussa** kohtaan **Moduulit > Ostoreskontra > Maksut > Maksukirjauskansio**.
11. Valitse **Rivit**.
12. Merkitse kaikki rivit tai poista kaikkien rivien merkinnät luettelossa.
13. Valitse **Maksun tila**.
14. Valitse **Ei mitään**.
15. Valitse **Muodosta maksut**.
16. Valitse **OK**.
17. Valitse **OK**. Analysoi luotu raportti. Huomaa, että luotu raportti on Word-muotoinen ja että siinä on käsiteltyjen maksujen tiedot.  
