---
title: Uuden kuljetuksenhallintamoduulin luominen
description: Tässä aiheessa kuvataan, miten luodaan uusi kuljetustenhallintamoduuli Dynamics 365 Supply Chain Managementissa.
author: Henrikan
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSGenericEngine, TMSRateEngine, TMSMileageEngine, TMSEngineParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: 51661
ms.assetid: 0473acef-755e-4b42-acf5-5e5aa902dc0e
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88661b6a974e2bd60f78e38d49a08d3290008b8b
ms.sourcegitcommit: 614d79cba238e466d445767a7d0a012e785a9861
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/19/2021
ms.locfileid: "7651986"
---
# <a name="create-a-new-transportation-management-engine"></a>Uuden kuljetuksenhallintamoduulin luominen

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan, miten luodaan uusi kuljetustenhallintamoduuli Dynamics 365 Supply Chain Managementissa. 

Kuljetustenhallinnan(TMS) moduulit määrittävät logiikan, jota käytetään kuljetushintojen luomiseen ja käsittelemiseen Kuljetuksenhallinnassa. Supply Chain Management tarjoaa useita eri moduulityyppejä, jotka laskevat erilaisia parametreja, kuten hintoja, kuljetusaikoja ja kuljetuksessa ylitettävien vyöhykkeiden määriä. Tässä artikkelissa kerrotaan, miten Microsoft Visual Studio -kehitysympäristöä ja Supply Chain Managementin kehitystyökaluja käytetään uuden TMS-moduulin luontiin ja käyttöönottoon ja miten moduuli sitten määritetään Operationsissa. Lisätietoja moduuleista: [Kuljetustenhallintamoduulit](transportation-management-engines.md).

## <a name="create-a-new-tms-engine"></a>Uuden TMS-moduulin luonti

Tässä osassa kerrotaan, miten luodaan luokkakirjasto, jossa on TMS-moduulin toteutus, ja miten siihen viitataan Supply Chain Management -mallista.

1. Uusien moduulien käyttöönottoa varten on oltava malli, johon moduulit sijoitetaan. Luo uusi malli valitsemalla **Dynamics 365** &gt; **Mallinhallinta** -valikossa **Luo malli**. Anna ohjatun **Luo malli** -toiminnon ensimmäisellä sivulla mallin nimeksi **TMSEngines**. 

   [![Mallin luominen.](./media/012.png)](./media/012.png)

2. Valitse seuraavalla sivulla **Luo uusi paketti**. 

   [![Uuden paketin luominen.](./media/021.png)](./media/021.png)

3. Valitse seuraavalla sivulla viitemalliksi **ApplicationSuite**. (**ApplicationPlatform**-malli on esivalittuna.) 

   [![Viitemallin valinta.](./media/032.png)](./media/032.png)

4. Vahvista uuden mallin luonti seuraavalla sivulla valitsemalla **Valmis**. 

   [![Mallin luomisen viimeistely.](./media/042.png)](./media/042.png)

5. Luo uudessa ratkaisussa uusi Supply Chain Management -projekti ja anna sille nimeksi **TMSThirdParty**. Määritä projektin ominaisuuksissa projektin malliksi **TMSEngines**.
6. Lisää ratkaisuun uusi C\#-luokkakirjasto ja anna sille nimeksi **ThirdPartyTMSEngines**.
7. Lisää ThirdPartyTMSEngines-projektissa viittaukset Supply Chain Management -kohtaisiin kokoonpanoihin:
   -   Sovelluskokoonpanot, joissa voi viitata X++-tyyppeihin. Näitä kokoonpanoja löytyy seuraavista sijainneista. \[Pakettien pääpolku\] on sen sijainnin polku, johon kaikki käyttöönotetut kokoonpanot sijoitetaan, kuten C:\\Paketit.

        ```xpp
        [Packages root]\ApplicationPlatform\bin\Dynamics.AX.ApplicationPlatform.dll
        [Packages root]\ApplicationFoundation\bin\Dynamics.AX.ApplicationFoundation.dll
        [Packages root]\ApplicationSuite\bin\Dynamics.AX.ApplicationSuite.dll
        ```
        
   -   Kehyskokoonpanot, joissa voi käyttää tietoja, LINQiä ja aputoimintoja. Kaikki nämä kokoonpanot löytyvät sijainnista \[Pakettien pääpolku\]\\bin.

        ```xpp 
        Microsoft.Dynamics.ApplicationPlatform.Environment.dll
        Microsoft.Dynamics.AX.Data.Core.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.AdoNet.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.Interface.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.Msil.dll
        Microsoft.Dynamics.AX.Server.Core.dll
        Microsoft.Dynamics.AX.Xpp.AxShared.dll
        Microsoft.Dynamics.AX.Xpp.Support.dll
        ```

   -   TMS-ydinkokoonpano (joka sisältää moduulit) ja TMS-peruskokoonpano (joka sisältää apurit, vakiot, tiedonsiirtoluokkien määritelmät jne.). Näitä kokoonpanoja löytyy seuraavista sijainneista.

        ```xpp
        [Packages root]\ApplicationSuite\bin\Microsoft.Dynamics.AX.Tms.dll
        [Packages root]\ApplicationSuite\bin\Microsoft.Dynamics.AX.Tms.Base.dll
        ```
8. Nimeä ThirdPartyTMSEngines-projektissa automaattisesti luotu C\#-luokan uudelleen muotoon **SampleRatingEngine**.
9. Toteuta moduuli. Koska tässä esimerkissä luodaan hintamoduuli, se perustuu hintamoduulien perusluokkaan. Perusluokka toteuttaa suurimman osan hintamoduuliliittymästä (**TMSFwkIRateEngine**). Meidän on vain toteutettava hintamenetelmä. Jotta esimerkki pysyisi yksinkertaisena, menetelmä rekisteröi kiinteästi koodatun hinnan 100. Voit luoda moduuleja, jotka toteuttavat mitä tahansa moduuliliittymiä (esim. **TMSFwkIAccessorialEngine**). Kaikki moduuliliittymät on määritetty X++:lla.

    ```xpp
    namespace ThirdPartyTMSEngines
    {
        using Dynamics.AX.Application;
        using Microsoft.Dynamics.Ax.Tms.Base.Data;
        using Microsoft.Dynamics.Ax.Tms.Base.Utility;
        using Microsoft.Dynamics.Ax.Tms.Bll;
        using System.Xml.Linq;
        public class SampleRatingEngine : BaseRateEngine
        {
            public override RatingDto rate(TmsTransactionFacade transactionFacade, XElement shipment, TMSRateMasterCode rateMasterCode)
            {
               XElement re = shipment.RetrieveOrCreateRatingEntity(this.RatingDto);
               re.AddRate(TmsRateType.Rate, 100);
               return this.RatingDto;
            }
        }
    }
    ```

10. Luo ratkaisu.
11. Lisää uusi viite TMSThirdParty-projektiin. Viitteen pitäisi viitata ThirdPartyTMSEngines-projektiin. Kun olet valmis, ratkaisun pitäisi näyttää tältä. 

    [![Ratkaisu, joka sisältää viitteen TMSThirdParty-projektiin.](./media/052.png)](./media/052.png)

12. Luo ratkaisu. Varmista, että uusi kirjasto näkyy sovellusten hallinnan **Viitteet**-solmussa. 

    [![Uusi kirjasto sovellusten hallinnan Viitteet-solmmussa.](./media/061.png)](./media/061.png)

## <a name="deploy-the-tms-engine-as-a-package"></a>TMS-moduulin toteutus pakettina

Yksi tapa ottaa käyttöön kolmannen osapuolen TMS-moduuleja on käyttää käyttöönottopakettia. Tätä menetelmää suositellaan tuotantoympäristössä. Kehitysympäristössä voit kopioida kokoonpanot manuaalisesti, kuten seuraavassa osassa TMS-moduulin määrittäminen Supply Chain Managementissa kuvataan. Moduuli otetaan käyttöön pakettina seuraavasti.

1. Valitse **Dynamics 365** &gt; **Käyttöönotto** -valikossa <strong>Luo käyttöönottopaketti</strong>.
2. Valitse **Luo käyttöönottopaketti**-valintaikkunassa TMSEngines-malli ja syötä polku, johon haluat tallentaa pakettitiedostot. 

   [![TMSEngines-mallin valitseminen.](./media/071.png)](./media/071.png)

3. Voit nyt ottaa paketin käyttöön kohdeympäristössä. Opasohjelma: [Käyttöönotettavan paketin asennus](../../fin-ops-core/dev-itpro/deployment/install-deployable-package.md).

## <a name="set-up-the-tms-engine-in-supply-chain-management"></a>TMS-moduulin määrittäminen Supply Chain Managementissa

Tässä osassa kerrotaan, miten Supply Chain Management määritetään käyttämään TMS-moduulia, ja esitetään, miten uutta luotua moduulia käytetään hintojen haussa. Tämän osan esimerkissä käytettään esittelytietojen USMF-yritystä.

1. Luo uusi moduuli Uuden TMS-moduulin luonti -osan mukaisesti.
2. Luo ratkaisu.
3. Kopioi tuloksena oleva kokoonpano Supply Chain Managementin palvelimen binaarisijaintiin \[AOSWebRoot\]bin. **Huomautus:** Tämä vaihe pätee vain kehitysympäristössä. Tuotantoympäristössä käyttöönotto kannattaa suorittaa käyttöönottopaketilla. Lisätietoja on edellisessä osassa TMS-moduulin toteutus pakettina.
4. Luo uusi hinnoittelumoduuli Supply Chain Managementin **Hintamoduulit**-sivulla. Moduulin pitäisi viitata moduulikokoonpanoon, joka tuotetaan luomalla moduuliluokkakirjasto ja käyttöönotettu moduuliluokka. 

   [![Uuden hinnoittelumoduulin luominen Hintamoduulit-sivulla.](./media/081.png)](./media/081.png)

5. Luo lähetyksen rahdinkuljettaja, joka käyttää esimerkkihintamoduulia. Koska moduuli ei käytä mitään tietoja, sinun ei tarvitse määrittää hinnan päätietoja. 

   [![Uuden lähetyksen rahdinkuljettajan luominen.](./media/092.png)](./media/092.png)

6. Valitse **Hinnan ja reitin työtila**-sivulla **Hintavertailu**. SampleCarrier-hinnan pitäisi olla 100.00, kuten seuraavassa näyttökuvassa. Tässä esimerkissä ostamme reitin varastosta 24 asiakkaalle US-004. Koska hinta kuitenkin on kiinteästi koodattu, näet aina hinnan 100.00.

   [![Hinnan ja reitin työtila.](./media/101.png)](./media/101.png)

## <a name="tips-and-tricks"></a>Vinkkejä ja niksejä

- Jos käytät Supply Chain Managementin kehitystyökaluja, ratkaisuun kannattaa lisätä uusi projekti. Jos määrität tämän projektin käynnistysprojektiksi ja aloitat virheenkorjausistunnon, voit tehdä virheenkorjauksen sekä X++- että C\#-koodin virheenkorjauksen samassa istunnossa.
- Aina kun muutat ThirdPartyTMSEngines-projektia ja käännät sen uudelleen, sinun on kopioitava tuloksena oleva kokoonpano manuaalisesti binaarisijaintiin tai käyttää käyttöönottoon käyttöönottopakettia. Muussa tapauksessa voit joutua suorittamaan vanhentuneella kokoonpanolla.
- Kun olet suorittanut TMS-kohtaisia toimintoja Supply Chain Managementissa, Internet Information Servicesin (IIS) työntekijäprosessi saattaa lukita ThirdPartyTMSEngines-kokoonpanon siten, että kokoonpanoa ei voi päivittää. Käynnistä tässä tapauksessa w3svc-prosessi uudelleen.

### <a name="whitepaper"></a>Tekninen raportti

Lisätietoja saa lataamalla seuraava tekninen raportti (joka on kirjoitettu tukemaan AX2012-versiota, mutta koskee myös Dynamics 365 Supply Chain Managementia)

- [Kuljetuksen hallintamoduulien toteuttaminen ja käyttöönotto](https://download.microsoft.com/download/b/5/f/b5ff8fef-3918-4c1d-92d5-b67eb0971684/ImplementingAndDeployingTransportationManagementEnginesInAX.pdf)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]