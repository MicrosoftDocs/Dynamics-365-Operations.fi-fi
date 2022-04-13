---
title: Laajennettujen kirjautumisten ominaisuuden lisääminen ja käyttö
description: Tässä ohjeaiheessa kuvataan, kuinka Microsoft Dynamics 365 Commercen myyntipistesovelluksen (POS) laajennettu kirjautumisominaisuus määritetään ja käytetään.
author: boycez
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: boycez
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: d211ecfe1550f6093e1d35e7c2b37c036b50dd4a
ms.sourcegitcommit: 5aebb181004eb63210503fb566dcda5c55032bee
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/29/2022
ms.locfileid: "8491436"
---
# <a name="set-up-and-use-the-extended-logon-capability"></a>Laajennettujen kirjautumisten ominaisuuden lisääminen ja käyttö

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kuvataan, kuinka Microsoft Dynamics 365 Commercen myyntipistesovelluksen (POS) laajennettu kirjautumisominaisuus määritetään ja käytetään.

Cloud POS (CPOS) ja Modern POS (MPOS) tarjoavat laajennetun sisäänkirjautumisominaisuuden, jonka avulla vähittäismyynnin työntekijät kirjautuvat POS-sovellukseen skannaamalla viivakoodin tai kortin magneettinauhan lukulaitteen avulla.

## <a name="set-up-extended-logon"></a>Jatketun sisäänkirjautumisen määrittäminen

Noudattamalla seuraavia ohjeita voit määrittää vähittäismyynnin POS-kassakomentoja varten laajennetun sisäänkirjauksen.

1. Siirry Commerce headquartersissa kohtaan **Retail ja Commerce \> Kanavan asetukset \> POS-asetukset \> POS-profiilit \> Toimintoprofiilit**. 
2. Valitse vasemmanpuoleisesta siirtymisruudusta vähittäismyyntisäilöön liittyvä toimintoprofiili.
3. Määritä **Toiminnot**-pikavälilehden **Kirjautumisen lisätodennusvaihtoehdot** -kohdassa **Kyllä**- tai **Ei**-asetus:

    - **Henkilökunnan viivakoodikirjautuminen** – Määritä tämän asetuksen arvoksi **Kyllä**, jos haluat, että työntekijät kirjautuvat myyntipisteeseen skannaamalla viivakoodin. 
    - **Henkilökunnan viivakoodikirjautuminen vaatii salasanaa** – Määritä tämän asetuksen arvoksi **Kyllä**, jos haluat, että työntekijät syöttävät salasanan kirjautuessaan myyntipisteeseen skannaamalla viivakoodin.
    - **Henkilökuntakorttikirjautuminen** – Määritä tämän asetuksen arvoksi **Kyllä**, jos haluat, että työntekijät kirjautuvat myyntipisteeseen pyyhkäisemällä korttia.
    - **Henkilökunnan korttikirjautuminen vaatii salasanaa** – Määritä tämän asetuksen arvoksi **Kyllä**, jos haluat, että työntekijät syöttävät salasanan kirjautuessaan myyntipisteeseen pyyhkäisemällä korttia.

Viivakoodi tai kortti liitetään tunnistetietoihin, jotka työntekijälle voidaan määrittää. Tunnistetiedoissa on oltava vähintään kuusi merkkiä. Merkkijono, joka sisältää viisi ensimmäistä merkkiä, on oltava yksilöivä, ja sitä pidetään *tunnistetietotunnuksena*, jota käytetään työntekijän hakuun. Muita merkkejä käytetään suojauksen vahvistuksessa. Oletetaan esimerkiksi, että sinulla on kaksi korttia, joista toisen tunnistetieto on 12345DGYDEYTDW sekä toinen, jonka on tunnistetieto on 12345EWUTBDAJH. Koska näillä korteilla on sama tunnistetietotunnus 12345, niitä ei voi määrittää työntekijöille onnistuneesti.

## <a name="assign-extended-logon"></a>Määritä jatkettu kirjautuminen

Oletuksena vain päälliköt voivat määrittää työntekijöille jatketun sisäänkirjautumisen. Määritä laajennettu sisäänkirjautuminen, siirtymällä myyntipisteessä kohtaan **Jatkettu kirjautuminen**. Etsi sitten työntekijä syöttämällä hänen operaattorintunnus hakukenttään. Valitse työntekijä ja napsauta sitten **Määritä**. Lue tai skannaa työntekijälle määritettävä jatkettu sisäänkirjautuminen seuraavalla sivulla. Jos kortin luku tai skannaus luettiin onnistuneesti, **OK**-painike tulee näkyviin. Napsauta **OK** tallentaaksesi jatkettu sisäänkirjautuminen kyseiselle työntekijälle.

## <a name="delete-extended-logon"></a>Poista jatkettu sisäänkirjautuminen

Poista työntekijälle määritetty jatkettu sisäänkirjautuminen etsimällä työntekijä **Jatkettu kirjautuminen** -toiminnon avulla. Valitse työntekijä ja napsauta sitten **Poista määritys**. Kaikki tälle käyttäjälle määritetyt jatketun kirjautumisen tunnistetiedot poistetaan.

## <a name="use-extended-logon"></a>Käytä jatkettua sisäänkirjautumista

Kun laajennettu kirjautuminen on määritetty ja työntekijälle on määritetty viivakoodi tai magneettiraita, työntekijän täytyy vain pyyhkäistä tai skannata korttiaan, kun POS-kirjautumissivu on näkyvissä. Jos tarvitaan myös salasana ennen kuin kirjautuminen voi jatkua, työntekijää kehotetaan syöttämään salasanansa.

## <a name="extend-extended-logon"></a>Laajenna jatkettua kirjautumista

Laajennetun sisäänkirjautumisominaisuuden käyttöönotto edellyttää, että tunnistetietojen vähimmäispituus on kuusi merkkiä ja että ensimmäiset viisi merkkiä (tunnistetietotunnus) ovat yksilöiviä. Se on alun perin tarkoitettu otokseksi, jonka kehittäjät voivat mukauttaa vastaamaan tietyn toteutuksen vaatimuksia. (Sitä voidaan esimerkiksi mukauttaa niin, että se tukee enemmän merkkejä tai käyttää erilaisia suojausvarmennussääntöjä.) Lisätietoja laajennuksien rakentamisesta laajennettua kirjautumista varten on kohdassa [MPOS- ja Cloud POS -laajennusten laajennetun kirjautumistoiminnon lisääminen](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/12/14/extending-the-extended-logon-functionality-for-mpos-and-cloud-pos/).

Kirjautumispalvelua voidaan myös laajentaa niin, että ne tukevat laajennettuja kirjautumislaitteita kuten käsiskannereita. Lisätietoja on [POS-laajennettavuusdokumentaatiossa](dev-itpro/pos-extension/pos-extension-overview.md).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
