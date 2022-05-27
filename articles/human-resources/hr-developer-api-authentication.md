---
title: Todennus
description: Tässä artikkelissa on yleistietoja käyttöoikeuksien todennuksesta Microsoft Dynamics 365 Human Resourcesin datasovelluksen ohjelmointirajapinnasta.
author: twheeloc
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 973bfd3582db1be7139042e9473efb833d6c9e8c
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687020"
---
# <a name="authentication"></a>Todennus


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä artikkelissa on yleistietoja käyttöoikeuksien todennuksesta Microsoft Dynamics 365 Human Resourcesin datasovelluksen ohjelmointirajapinnasta.

## <a name="overview"></a>Yleiskatsaus

Henkilöresurssien dataohjelmointirajapinta on OData-toteutus. Lisätietoja on kohdassa [Open Data Protocol (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md).

Sovellus on todennettava valtuutettuna soittajana, ennen kuin ohjelmointirajapintapalvelu hakee sovelluspyyntöjä.

## <a name="fundamentals"></a>Perusteet

Jotta voisit soittaa dataohjelmointirajapintaliittymään, sovelluksen on hankittava käyttötunnus Microsoftin käyttäjätietoympäristöstä. Käyttötunnussanoma sisältää sovelluksen tiedot sekä käyttöoikeudet, jotka sen on kutsuttava henkilöstöhallintaan.

### <a name="access-token"></a>Käyttöoikeustietue

Microsoftin käyttäjätietoympäristön myöntämiä käyttöoikeustunnuksia ovat base64 -koodatut JavaScript Object Notation (JSON) -webtunnukset (JWT). Ne sisältävät tietoja (väitteitä), joiden mukaan dataohjelmointirajapinta (ja muut Internet-ohjelmointirajapintaliittymät, jotka on suojattu Microsoftin käyttäjätietoympäristöalustalla) käyttää vahvistukseen soittajaa ja varmistaa, että kutsujalla on oikeat käyttöoikeudet pyytämiensä toimintojen suorittamiseen. Puheluissa voit käsitellä käyttötunnuksia läpinäkymättöminä. Siirtotunnukset on aina lähetettävä suojatun kanavan kautta, esimerkiksi Transport Layer Security (TLS) - ja Hypertext Transfer Protocol Secure (HTTPS) -protokollan avulla.

Tässä on esimerkki Microsoftin käyttäjätietoympäristön myöntämästä käyttöoikeustunnuksesta.

```jwt
EwAoA8l6BAAU7p9QDpi/D7xJLwsTgCg3TskyTaQAAXu71AU9f4aS4rOK5xoO/SU5HZKSXtCsDe0Pj7uSc5Ug008qTI+a9M1tBeKoTs7tHzhJNSKgk7pm5e8d3oGWXX5shyOG3cKSqgfwuNDnmmPDNDivwmi9kmKqWIC9OQRf8InpYXH7NdUYNwN+jljffvNTewdZz42VPrvqoMH7hSxiG7A1h8leOv4F3Ek/oeJX6U8nnL9nJ5pHLVuPWD0aNnTPTJD8Y4oQTp5zLhDIIfaJCaGcQperULVF7K6yX8MhHxIBwek418rKIp11om0SWBXOYSGOM0rNNN59qNiKwLNK+MPUf7ObcRBN5I5vg8jB7IMoz66jrNmT2uiWCyI8MmYDZgAACPoaZ9REyqke+AE1/x1ZX0w7OamUexKF8YGZiw+cDpT/BP1GsONnwI4a8M7HsBtDgZPRd6/Hfqlq3HE2xLuhYX8bAc1MUr0gP9KuH6HDQNlIV4KaRZWxyRo1wmKHOF5G5wTHrtxg8tnXylMc1PKOtaXIU4JJZ1l4x/7FwhPmg9M86PBPWr5zwUj2CVXC7wWlL/6M89Mlh8yXESMO3AIuAmEMKjqauPrgi9hAdI2oqnLZWCRL9gcHBida1y0DTXQhcwMv1ORrk65VFHtVgYAegrxu3NDoJiDyVaPZxDwTYRGjPII3va8GALAMVy5xou2ikzRvJjW7Gm3XoaqJCTCExN4m5i/Dqc81Gr4uT7OaeypYTUjnwCh7aMhsOTDJehefzjXhlkn//2eik+NivKx/BTJBEdT6MR97Wh/ns/VcK7QTmbjwbU2cwLngT7Ylq+uzhx54R9JMaSLhnw+/nIrcVkG77Hi3neShKeZmnl5DC9PuwIbtNvVge3Q+V0ws2zsL3z7ndz4tTMYFdvR/XbrnbEErTDLWrV6Lc3JHQMs0bYUyTBg5dThwCiuZ1evaT6BlMMLuSCVxdBGzXTBcvGwihFzZbyNoX+52DS5x+RbIEvd6KWOpQ6Ni+1GAawHDdNUiQTQFXRxLSHfc9fh7hE4qcD7PqHGsykYj7A0XqHCjbKKgWSkcAg==
```

Jos haluat soittaa dataohjelmointirajapintaliittymään, liitä käyttöoikeustietue merkiksi HTTP-pyynnön valtuutustietoihin. Esimerkki:

```HTTP
HTTP/1.1
Authorization: Bearer EwAoA8l6BAAU ... 7PqHGsykYj7A0XqHCjbKKgWSkcAg==
Host: https://{cluster}.hr.talent.dynamics.com
GET https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/JobTypes
```

## <a name="register-a-new-application-by-using-the-azure-portal"></a>Rekisteröi uusi sovellus Azure-portaalissa

1. Kirjaudu [Microsoft Azure -portaaliin](https://portal.azure.com) työ- tai koulutilillä tai henkilökohtaisella Microsoft-tilillä.

2. Jos tilin avulla voit käyttää useita vuokralaisia, valitse tilisi oikeasta yläkulmasta ja aseta portaali-istunto Azure Active Directory (Azure AD) haluamallesi vuokralaiselle.

3. Valitse **Azure Active Directory** -palvelu vasemmanpuoleisesta ruudusta ja valitse sitten **Sovellusrekisteröinnit \> Uusi rekisteröinti**.

4. Kun **Rekisteröi sovellus** -sivu tulee näkyviin, kirjoita sovelluksen rekisteröintitiedot:

    - **Nimi**: Anna mielekäs sovelluksen nimi, joka näytetään sovelluksen käyttäjille.
    - **Tuetut tilityypit**: Valitse tilityypit, joita sovelluksesi tukee.

        | Tuetut tilityypit | Kuvaus |
        |-------------------------|-------------|
        | Vain tämän organisaation hakemiston tilit | Valitse tämä vaihtoehto, jos olet rakentamassa yrityssovellusta. Tämä vaihtoehto ei ole käytettävissä, ellet ole rekisteröimässä sovellusta hakemistossa.<p>Tämä vaihtoehto on liitetty vain yhteen **Azure AD:n vuokralaiseen**.</p><p>Tämä vaihtoehto on oletusasetus, ellet ole rekisteröimässä sovellusta hakemiston ulkopuolelle. Tässä tapauksessa oletusvaihtoehto on useat **Azure AD:n vuokralaiset ja henkilökohtaisen Microsoft-tilit**.</p> |
        | Minkä tahansa organisaation hakemiston tilit | Valitse tämä vaihtoehto, jos haluat kohdistaa kaikki liike- ja koulutusasiakkaat.<p>Tämä vaihtoehto on liitetty useisiin **Azure AD:n vuokralaisiin**.</p><p>Jos olet rekisteröinyt sovelluksen **Azure AD:na vain yhden vuokralaisen käyttöön**, voit päivittää sen **Azure AD:ksi vain usean vuokralaisen käyttöön** ja sitten takaisin **Azure AD:ksi vain yhden vuokralaisen käyttöön** **Todennus**-lavan avulla.</p> |
        | Tilit missä tahansa organisaatiohakemistossa ja omissa Microsoft-tileissä | Valitse tämä vaihtoehto, kun haluat kohdistaa laajimman asiakasjoukon.<p>Tämä vaihtoehto on yhdistetty useisiin **Azure AD:n vuokralaisiin ja henkilökohtaisiin Microsoft-tileihin**.</p><p>Jos olet rekisteröinyt sovelluksen **Azure AD:n usean vuokralaisen ja henkilökohtaisen Microsoft-tilisi** käyttäjäksi, et voi muuttaa tätä asetusta käyttöliittymässä. Sen sijaan on käytettävä sovelluksen luetteloeditoria tuettujen tilityyppien muuttamiseen.</p> |

    - **Uudelleenohjauksen URI (valinnainen)** – Valitse sen sovelluksen tyyppi, jota olet rakentamassa: **Verkko**- tai **Julkinen asiakasohjelma (mobiili & työpöytä**). Kirjoita sitten sovelluksen uudelleenohjauksen URI (tai vastaus-URL).

        - Jos kyseessä on Internet-sovellus, anna sovelluksen perusosoite. Tämä `http://localhost:31544` voi olla esimerkiksi paikallisessa tietokoneessa käytettävän Internet-sovelluksen URL-osoite. Tämän jälkeen käyttäjät kirjautuvat WWW-asiakasohjelmaan tämän URL-osoitteen avulla.
        - Jos kyseessä on yleinen asiakassovellus, anna URI-tunnus, jota Azure AD käyttää palauttamaan tunnuksen vastauksia. Kirjoita sovellukseen liittyviä arvoja, kuten `myapp://auth`.

        Lisätietoja Internet-sovelluksista ja alkuperäisistä sovelluksista on [Microsoftin käyttäjätietoympäristössä (aiemmin Azure Active Directory sovelluskehittäjille)](/azure/active-directory/develop/#quickstarts).

5. Valitse **API-käyttöoikeudet**-kohdasta **Lisää käyttöoikeus**. Valitse sitten **API-liittymät, joita oma organisaationi käyttää** -välilehti, etsi **Dynamics 365 Human Resources** ja lisää **käyttäjä\_tekeytyminen**-oikeus sovellukseen. Henkilöstöhallinnon sovellustunnus on f9be0c49-aa22-4ec6-911a-c5da515226ff. Tämän tunnuksen avulla voit varmistaa, että olet valinnut oikean sovelluksen.

6. Valitse **Rekisteröi**.

   [![Uuden sovelluksen rekisteröiminen Azure-portaaliin.](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)

Azure AD määrittää sovellukseesi yksilöllisen sovellustunnuksen (asiakastunnus) ja vie sinut sovelluksesi **yhteenveto**-sivulle. Jos haluat lisätä sovellukseesi muita ominaisuuksia, voit valita muita asetuksia, kuten brändäyksen sekä sertifikaattien ja salaisuuksien asetukset.

## <a name="retrieving-an-access-token"></a>Käyttötunnussanoman noutaminen

Henkilöstöhallinnon dataohjelmointirajapintaliittymän kutsumiseen käytettävän käyttötunnussanoman tiedot määräytyvät sen mukaan, mitä tekniikoita asiakassovelluksen kehittämisessä käytetään. Voit esimerkiksi [kokeilla kolmannen osapuolen apuohjelmaa](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (kuten Postman), kehittää C#-konsolisovellusta tai Internet-palvelua tai rakentaa javascript/TypeScript-asiakasta.

Esimerkki C#-asiakassovelluksesta:
```C#
using System;
using System.Net.Http;
using System.Threading.Tasks;

// requires appropriate NuGet package references in the project
using Microsoft.IdentityModel.Clients.ActiveDirectory;

namespace TalentODataPoC
{
    class Program
    {
        // prereq: This client app must be registered in Azure Active Directory. The app must be
        // registered as requiring permission to the Dynamics 365 for Talent API (with the Dynamics
        // HCM Workload delegated permission).
        static string clientId = "4fc703ef-672c-4e2c-813f-2f9d29d726db"; // This value should be obtained from AAD and must match your registered app
        static string talentNamespaceUri = "";

        public static async Task CallTalentODataService()
        {
            // authority URI
            UriBuilder uri = new UriBuilder("https://login.microsoftonline.com/common");
            AuthenticationContext authenticationContext = new AuthenticationContext(uri.ToString());

            // request token for the resource we want to access (Human Resources). This will authenticate
            // the user and return an access token containing claims for the authenticated user.
            var authResult = await authenticationContext.AcquireTokenAsync(
                "http://hr.talent.dynamics.com", /*Talent app id or resource URI*/
                clientId, /*registered client app id*/
                new Uri("https://localhost"), /*redirect URI, as registered in your AAD app*/
                new PlatformParameters(PromptBehavior.SelectAccount));

            // create the authorization header, which needs to be passed in the Header of the HTTP Requests to Talent
            string authHeader = authResult.CreateAuthorizationHeader();

            // HINT: paste the JWT into https://jwt.ms to decode and view it
            Console.Write("authHeader: ");
            Console.WriteLine(authHeader);
            Console.WriteLine();

            HttpClient client = new HttpClient();
            client.DefaultRequestHeaders.Add("Authorization", authHeader);

            string s;

            Console.Write("Talent Namespace URI: ");
            Console.WriteLine(talentNamespaceUri);
            Console.WriteLine();

            // call the OData service to get JobType data from Talent
            var resultOdata = await client.GetAsync(talentNamespaceUri + "data/JobTypes");
            s = await resultOdata.Content.ReadAsStringAsync();
            Console.WriteLine(s);
            Console.WriteLine();
        }

        static void Main(string[] args)
        {
            Console.WriteLine();

            // if the user passes in a single parameter, assume it is the namespaceUri for Talent
            if (args.Length == 1)
            {
                talentNamespaceUri = args[0];
            } else if (args.Length == 0)
            {
                Console.WriteLine("Enter Talent URL including namespace.");
                Console.WriteLine("Example: https://aos-rts-sf-21454f9d830-prod-westus2.hr.talent.dynamics.com/namespaces/2328af1a-2d45-4c6a-99e3-12a4c3867dcf/");
                Console.Write("> ");
                talentNamespaceUri = Console.ReadLine();
                if (!talentNamespaceUri.EndsWith("/"))
                {
                    talentNamespaceUri = talentNamespaceUri + "/";
                }
            } else
            {
                Console.WriteLine("Unexpected Arguments");
                System.Environment.Exit(1);
            }

            Task t = Program.CallTalentODataService();
            t.Wait();
        }
    }
}
```

Kun olet hakenut käyttötunnussanoman, ohitat valtuutustietojen otsikossa olevan tunnuksen ja jokaisen pyynnön, jonka lähetät tietojen ohjelmointirajapintaliittymään edellä kuvatulla tavalla.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
