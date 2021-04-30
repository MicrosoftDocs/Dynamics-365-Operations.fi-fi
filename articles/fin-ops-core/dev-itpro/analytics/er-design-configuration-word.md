---
title: Uuden ER-määrityksen suunnitteleminen luomaan Word-muotoisia raportteja
description: Tässä aiheessa käsitellään tapaa, jolla käyttävät voivat määrittää uuden sähköisen raportoinnin (ER) muodon luomaan raportteja Microsoft Word -asiakirjoina.
author: NickSelin
ms.date: 12/17/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: 7790d7e581b9b4260a4c57af84b02a182dde953d
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5894073"
---
# <a name="design-a-new-er-configuration-to-generate-reports-in-word-format"></a>Uuden ER-määrityksen suunnitteleminen luomaan Word-muotoisia raportteja

[!include [banner](../includes/banner.md)]

Raporttien luominen Microsoft Word -asiakirjoina edellyttää, että raporteille suunnitellaan malli käyttämällä esimerkiksi Wordin työpöytäsovellusta. Seuraavassa kuvassa on esimerkkimalli valvontaraportista, joka voidaan luoda näyttämään käsiteltyjen toimittajamaksujen tiedot.

![Valvontaraportin esimerkkimalli Wordin työpöytäsovelluksessa](./media/er-design-configuration-word-image1.png)

Word-asiakirjaa voi käyttää Word-muotoisten raporttien mallina määrittämällä uuden [sähköisen raportoinnin (ER)](general-electronic-reporting.md) [ratkaisun](er-quick-start1-new-solution.md). Tässä ratkaisussa on oltava ER-[määritys](general-electronic-reporting.md#Configuration), joka sisältää ER-[muodon](general-electronic-reporting.md#FormatComponentOutbound) osan.

> [!NOTE]
> Kun uusi ER-muotomääritys luodaan muodostamaan Word-muotoisia raportteja, **Word** on joko valittava muodon tyypiksi avattavassa **Luo määritys** -valintaikkunassa tai **Muodon tyyppi** -kenttä on jätettävä tyhjäksi.

![Muodon määrityksen luominen Määritykset-sivulla](./media/er-design-configuration-word-image2.gif)

Ratkaisun ER-muoto-osan on sisällettävä **Excel\\Tiedosto**-muotoelementti, ja kyseinen muotoelementti on linkitettävä siihen Word-asiakirjaan, jota käytetään luotavien raporttien mallina suorituksen aikana. ER-muoto-osan määrittämistä varten on avattava luodun ER-määrityksen [luonnos](general-electronic-reporting.md#component-versioning) ER-muodon suunnittelutoiminnossa. Tämän jälkeen lisätään **Excel\\Tiedosto**-elementti, liitetään Word-malli muokattavaan ER-muotoon ja linkitetään kyseinen malli lisättyyn **Excel\\Tiedosto**-elementtiin.

> [!NOTE]
> Mallia liitettäessä on käytettävä [asiakirjatyyppiä](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types), joka on [määritetty](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) aiemmin ER-parametreissa tallentamaan ER-muotojen mallit.

![Mallin liittäminen Muodon suunnittelija -sivulla](./media/er-design-configuration-word-image3.gif)

Sisäkkäiset **Excel\\Alue**- ja **Excel\\Solu**-elementit voidaan lisätä **Excel\\Tiedosto**-elementtiin määrittämään niiden tietojen rakenne, jotka annetaan luotavissa raporteissa suorituksen aikana. Nämä elementit on sitten sidottava muokattavan ER-muodon tietolähteisiin, jotta niillä voidaan määrittää todelliset luotaviin raportteihin suorituksen aikana annettavat tiedot.

![Sisäkkäisten elementtien lisääminen Muodon suunnittelija -sivulla](./media/er-design-configuration-word-image4.gif)

Kun ER-muodon muutokset tallennetaan suunnittelun yhteydessä, muodon hierarkkinen rakenne tallennetaan liitettyyn Word-malliin **Raportti**-nimisenä [mukautettuna XML-osana](/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019). Mukautettuun malliin on siirryttävä ja se on ladattava Financesta, tallennettava paikallisesti ja avattava Wordin työpöytäsovelluksessa. Seuraavassa kuvassa paikallisesti tallennettu esimerkkimalli valvontaraportista, joka sisältää mukautetun **Raportti**-XML-osan.

![Raporttimalliesimerkin esikatselu Wordin työpöytäsovelluksessa](./media/er-design-configuration-word-image5.gif)

Kun **Excel\\Alue**- ja **Excel\\Solu**-muotoelementtien sidonnat suoritetaan suorituksen aikana, kunkin sidonnan tiedot tuodaan luotuihin Word-asiakirjoihin mukautetun **Raportti**-XML-osan yksittäisinä kenttinä. Mukautetun XML-osan kenttien arvojen antaminen luodussa asiakirjassa edellyttää, että soveltuvat Wordin [sisällön ohjausobjektit](/office/client-developer/word/content-controls-in-word) lisätään Word-malleihin suorituksen aikana täytettävien tietojen paikkamerkkeinä. Sisällön ohjausobjektien täyttäminen määritetään yhdistämällä jokainen sisällön ohjausobjekti sopivaan mukautetun **Raportti**-XML-osan kenttään.

![Sisällön ohjausobjektien lisääminen ja yhdistäminen Wordin työpöytäsovelluksessa](./media/er-design-configuration-word-image6.gif)

Muokattavan ER-muodon alkuperäinen Word-malli on sitten korvattava muokatulla mallilla, joka sisältää nyt mukautetun **Raportti**-XML-osan kenttiin yhdistetyt Wordin sisällön ohjausobjektit.

![Mallin korvaaminen Muodon suunnittelija -sivulla](./media/er-design-configuration-word-image7.gif)

Kun määritetty ER-muoto suoritetaan, liitettyä Word-mallia käytetään luomaan uusi raportti: Varsinaiset tiedot tallennetaan Word-raportin **Raportti**-nimisenä mukautettuna XML-osana. Kun luotu raportti avataan, Wordin sisällön ohjausobjekteihin täytetään mukautetun **Raportti**-XML-osan tiedot.

## <a name="frequently-asked-questions"></a>Usein kysytyt kysymykset

**Kysymys:** ER-muoto on määritetty tulostamaan yrityksen osoitteen sisältävä Word-asiakirja. Tämän ER-muodon Word-malliin on lisätty muotoiltu sisällön ohjausobjekti ilmaisemaan yrityksen osoite. Yrityksen osoite annettiin Financessa monirivisenä tekstinä ja rivinvaihto lisättiin **Enter**-näppäimellä. Yrityksen osoitteen pitäisikin tämän vuoksi näkyä monirivisenä tekstinä luoduissa asiakirjoissa. Osoite näkyy kuitenkin yhtenä tekstirivinä, joka sisältää erikoismerkkejä eikä rivinvaihtoja. Mitä vikaa asetuksessa on?

**Vastaus:** Muotoillun tekstisisällön ohjausobjektin sijaan on käytettävä vain teksti -muotoista sisällön ohjausobjektia ja valittava **Salli rivinvaihdot (useat kappaleet)** -valintaruutu ohjausobjektin ominaisuuksissa.

## <a name="additional-resources"></a>Lisäresurssit

- [Excel-malleja sisältävien ER-määritysten käyttäminen uudelleen Word-muotoisten raporttien luontiin](./tasks/er-design-configuration-word-2016-11.md)
- [Kuvien ja muotojen upottaminen luomiisi asiakirjoihin ER:n avulla](electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]