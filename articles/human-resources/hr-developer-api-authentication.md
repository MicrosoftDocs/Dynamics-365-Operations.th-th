---
title: การรับรองความถูกต้อง
description: บทความนี้แสดงข้อมูลภาพรวมเกี่ยวกับวิธีการรับรองความถูกต้องของข้อมูลอินเทอร์เฟสโปรแกรมประยุกต์ (API) ของ Microsoft Dynamics 365 Human Resources
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3dffe1db98ba39fde2229e69bc70bdbf113ff6ad
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793692"
---
# <a name="authentication"></a>การรับรองความถูกต้อง

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

บทความนี้แสดงข้อมูลภาพรวมเกี่ยวกับวิธีการรับรองความถูกต้องของข้อมูลอินเทอร์เฟสโปรแกรมประยุกต์ (API) ของ Microsoft Dynamics 365 Human Resources

## <a name="overview"></a>ภาพรวม

API ข้อมูลสำหรับทรัพยากรบุคคลเป็นการดำเนินการ OData สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [เปิดโพรโทคอลข้อมูล (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md)

ใบสมัครของคุณต้องรับรองความถูกต้องเป็นผู้เรียกที่ได้รับอนุญาตก่อนที่ API จะมีการร้องขอการบริการจากแอพลิเคชันของคุณ

## <a name="fundamentals"></a>พื้นฐาน

เมื่อต้องการเรียก API ข้อมูลแอพลิเคชันของคุณจะต้องได้รับการเข้าถึงจากแพลตฟอร์ม Microsoft identity โทเคนการเข้าถึงประกอบด้วยข้อมูลเกี่ยวกับใบสมัครของคุณและสิทธิ์การได้รับอนุญาตที่มีการเรียกทรัพยากรในทรัพยากรบุคคล

### <a name="access-token"></a>โทเคนการเข้าถึง

โทเคนการเข้าถึงที่ออกโดยแพลตฟอร์มข้อมูลเฉพาะของ Microsoft คือ base64 –การเข้ารหัสเว็บโทเคนโทเคน (JWTs) ของ JavaScript Object Notation (JSON) มีข้อมูล (การอ้างสิทธิ์) ที่ API ข้อมูล (และเว็บ APIs อื่นๆที่มีการรักษาความปลอดภัยโดยแพลตฟอร์ม Microsoft identity) ใช้เพื่อตรวจสอบความถูกต้องของผู้เรียกและตรวจสอบให้แน่ใจว่าผู้เรียกมีสิทธิ์ที่ถูกต้องในการดำเนินการที่ผู้ใช้เหล่านั้นกำลังร้องขอ ในระหว่างการเรียกคุณสามารถรักษาโทเคนการเข้าถึงเป็นแบบทึบ คุณควรส่งโทเคนการเข้าถึงไปยังช่องทางที่ปลอดภัย เช่น ความปลอดภัยการขนส่งเลเยอร์ (TLS) และความปลอดภัยของโพรโทคอลการโอนถ่ายข้อมูลแบบ Hypertext (HTTPS) 

ต่อไปนี้เป็นตัวอย่างของโทเคนการเข้าถึงที่ออกโดยแพลตฟอร์มข้อมูลเฉพาะของ Microsoft

```jwt
EwAoA8l6BAAU7p9QDpi/D7xJLwsTgCg3TskyTaQAAXu71AU9f4aS4rOK5xoO/SU5HZKSXtCsDe0Pj7uSc5Ug008qTI+a9M1tBeKoTs7tHzhJNSKgk7pm5e8d3oGWXX5shyOG3cKSqgfwuNDnmmPDNDivwmi9kmKqWIC9OQRf8InpYXH7NdUYNwN+jljffvNTewdZz42VPrvqoMH7hSxiG7A1h8leOv4F3Ek/oeJX6U8nnL9nJ5pHLVuPWD0aNnTPTJD8Y4oQTp5zLhDIIfaJCaGcQperULVF7K6yX8MhHxIBwek418rKIp11om0SWBXOYSGOM0rNNN59qNiKwLNK+MPUf7ObcRBN5I5vg8jB7IMoz66jrNmT2uiWCyI8MmYDZgAACPoaZ9REyqke+AE1/x1ZX0w7OamUexKF8YGZiw+cDpT/BP1GsONnwI4a8M7HsBtDgZPRd6/Hfqlq3HE2xLuhYX8bAc1MUr0gP9KuH6HDQNlIV4KaRZWxyRo1wmKHOF5G5wTHrtxg8tnXylMc1PKOtaXIU4JJZ1l4x/7FwhPmg9M86PBPWr5zwUj2CVXC7wWlL/6M89Mlh8yXESMO3AIuAmEMKjqauPrgi9hAdI2oqnLZWCRL9gcHBida1y0DTXQhcwMv1ORrk65VFHtVgYAegrxu3NDoJiDyVaPZxDwTYRGjPII3va8GALAMVy5xou2ikzRvJjW7Gm3XoaqJCTCExN4m5i/Dqc81Gr4uT7OaeypYTUjnwCh7aMhsOTDJehefzjXhlkn//2eik+NivKx/BTJBEdT6MR97Wh/ns/VcK7QTmbjwbU2cwLngT7Ylq+uzhx54R9JMaSLhnw+/nIrcVkG77Hi3neShKeZmnl5DC9PuwIbtNvVge3Q+V0ws2zsL3z7ndz4tTMYFdvR/XbrnbEErTDLWrV6Lc3JHQMs0bYUyTBg5dThwCiuZ1evaT6BlMMLuSCVxdBGzXTBcvGwihFzZbyNoX+52DS5x+RbIEvd6KWOpQ6Ni+1GAawHDdNUiQTQFXRxLSHfc9fh7hE4qcD7PqHGsykYj7A0XqHCjbKKgWSkcAg==
```

เมื่อต้องการเรียก API ข้อมูล คุณต้องแนบโทเคนการเข้าถึงเป็นโทเคนผู้ถือสิทธิ์ไปยังหัวข้อการตรวจสอบในการร้องขอ HTTP ของคุณ นี่คือตัวอย่าง

```HTTP
HTTP/1.1
Authorization: Bearer EwAoA8l6BAAU ... 7PqHGsykYj7A0XqHCjbKKgWSkcAg==
Host: https://{cluster}.hr.talent.dynamics.com
GET https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/JobTypes
```

## <a name="register-a-new-application-by-using-the-azure-portal"></a>ลงทะเบียนแอปพลิเคชันใหม่โดยใช้พอร์ทัล Azure

1. ล็อกอินไปยัง [พอร์ทัล Microsoft Azure](https://portal.azure.com) ที่มีบัญชีที่ทำงานหรือโรงเรียนหรือบัญชี Microsoft ส่วนบุคคล

2. ถ้าบัญชีของคุณให้สิทธิการเข้าถึงแก่ผู้เช่ามากกว่าหนึ่งราย ให้เลือกบัญชีของคุณในมุมด้านขวาบน และตั้งค่ารอบของพอร์ทัลไปยังผู้เช่า Azure Active Directory (Azure AD) ที่คุณต้องการ

3. ในบานหน้าต่างด้านซ้าย ให้เลือกบริการ **Azure Active Directory** แล้วเลือก **การลงทะเบียนแอป \> ลงทะเบียนใหม่**

4. เมื่อหน้า **ลงทะเบียนแอปพลิเคชัน** ปรากฏขึ้น ให้ป้อนข้อมูลการลงทะเบียนของแอพลิเคชันของคุณ:

    - **ชื่อ**: ให้ป้อนชื่อที่มีความหมายของแอปพลิเคชันที่จะแสดงต่อผู้ใช้แอปพลิเคชัน
    - **ชนิดบัญชีที่ได้รับการสนับสนุน**: เลือกชนิดบัญชีที่แอปของคุณควรสนับสนุน

        | ชนิดบัญชีที่ได้รับการสนับสนุน | คำอธิบาย |
        |-------------------------|-------------|
        | บัญชีในไดเรกทอรีขององค์กรนี้เท่านั้น | เลือกตัวเลือกนี้ถ้าคุณกำลังสร้างแอปพลิเคชันสายธุรกิจ ตัวเลือกนี้จะไม่พร้อมใช้งานจนกว่าคุณจะลงทะเบียนแอปในไดเรกทอรี<p>ตัวเลือกนี้จะถูกแม็ปกับ **ผู้เช่า Azure AD คนเดียวเท่านั้น**</p><p>ตัวเลือกนี้เป็นตัวเลือกเริ่มต้นยกเว้นว่าคุณกำลังลงทะเบียนแอปพลิเคภายนอกไดเรกทอรี ในกรณีนี้ ตัวเลือกเริ่มต้นคือผู้เช่า **Azure AD หลายรายและบัญชีส่วนบุคคล Microsoft**</p> |
        | บัญชีในไดเรกทอรีขององค์กรใดๆ | เลือกตัวเลือกนี้เพื่อกำหนดเป้าหมายลูกค้าธุรกิจและการศึกษาทั้งหมด<p>ตัวเลือกนี้จะถูกแม็ปกับ **ผู้เช่า Azure AD มากกว่าหนึ่งคนเท่านั้น**</p><p>ถ้าคุณลงทะเบียนแอป **ผู้เช่า Azure AD รายเดียวเท่านั้น** คุณสามารถใช้เบลด **การรับรองความถูกต้อง** เพื่ออัพเดตเป็น **ผู้เช่า Azure AD มากกว่าหนึ่งรายเท่านั้น** และกลับไปยัง **ผู้เช่า Azure AD รายเดียวเท่านั้น**</p> |
        | บัญชีในไดเรกทอรีขององค์กรและบัญชี Microsoft ส่วนบุคคล | เลือกตัวเลือกนี้เพื่อกำหนดเป้าหมายของกลุ่มลูกค้าที่กว้างที่สุด<p>ตัวเลือกนี้ถูกแม็ปโดย **ผู้เช่า Azure AD หลายรายเท่านั้นและบัญชีส่วนบุคคล Microsoft**</p><p>ถ้าคุณลงทะเบียนแอป **ผู้เช่า Azure AD หลายรายและบัญชี Microsoft ส่วนบุคคล** คุณจะไม่สามารถเปลี่ยนการตั้งค่านี้ในอินเทอร์เฟสผู้ใช้ (UI) ได้ ในทางกลับกัน คุณต้องใช้ตัวแก้ไขรายการแอปพลิเคชันเพื่อเปลี่ยนชนิดบัญชีที่ได้รับการสนับสนุน</p> |

    - **การเปลี่ยนเส้นทาง URI (ตัวเลือก)** – เลือกชนิดของแอปที่คุณกำลังสร้าง **เว็บ** หรือ **ไคลเอนต์สาธารณะ (บนมือถือ & เดสก์ทอป)** ป้อน URI ที่เปลี่ยนเส้นทาง (หรือตอบกลับ URL)  สำหรับแอปพลิเคชัน

        - สำหรับแอปเว็บ ระบุ URL พื้นฐานของแอป ตัวอย่างเช่น `http://localhost:31544` อาจเป็น URL สำหรับเว็บแอปพลิเคชันที่ดำเนินการบนเครื่องเฉพาะที่ของคุณ จากนั้น ผู้ใช้ใช้ URL นี้เพื่อล็อกอินไปยังแอปพลิเคชันไคลเอนต์ของเว็บ
        - สำหรับแอปพลิเคชันไคลเอนต์สาธารณะให้ URL ที่ Azure AD ใช้เพื่อส่งคืนการตอบสนองโทเคน ป้อนค่าที่เกี่ยวข้องกับแอปของคุณโดยเฉพาะเช่น`myapp://auth`

        เมื่อต้องการดูตัวอย่างเฉพาะสำหรับ web apps หรือแอปพลิเคชันดังเดิม ให้ดูที่ quickstarts ใน [แพลตฟอร์ม Microsoft identity (Azure Active Directory เดิมสำหรับนักพัฒนา)](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts)

5. ภายใต้ **สิทธิ์ของ API** ให้เลือก **เพิ่มสิทธิการได้รับอนุญาต** จากนั้น บนแท็บ **APIs องค์กรของฉันใช้** ให้ค้นหา **Dynamics 365 Human Resources** และเพิ่มสิทธิ์ **ผู้ใช้\_การเลียนแบบ** กับแอปของคุณ รหัสแอปพลิเคชันสำหรับทรัพยากรบุคคลคือ f9be0c49-aa22-4ec6-911a-c5da515226ff ใช้รหัสนี้เพื่อให้แน่ใจว่าคุณได้เลือกแอปพลิเคชันที่ถูกต้อง

6. เลือก **การลงทะเบียน**

   [![กำลังลงทะเบียนแอปใหม่ในพอร์ทัล Azure](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)

Azure AD กำหนดรหัสแอปพลิเคชันเฉพาะ (รหัสไคลเอนต์) ให้กับแอปของคุณและ นำคุณไปยังหน้า **ภาพรวม** สำหรับแอปของคุณ เพื่อเพิ่มความสามารถไปยังแอปของคุณ คุณสามารถเลือกการตั้งค่าคอนฟิกอื่นๆ เช่น ตัวเลือกสำหรับการสร้างแบรนด์ และสำหรับใบรับรองและความลับ

## <a name="retrieving-an-access-token"></a>การดึงข้อมูลโทเคนการเข้าถึง

ข้อกำหนดในการดึงข้อมูลโทเคนการเข้าถึงสำหรับการเรียก API ข้อมูลทรัพยากรบุคคลจะขึ้นอยู่กับเทคโนโลยีที่คุณกำลังใช้ในการพัฒนาแอปพลิเคชันไคลเอนต์ของคุณ ตัวอย่างเช่น คุณอาจ [กำลังทดสอบกับยูทิลิตี้](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (เช่นบุรุษไปรษณีย์) การพัฒนาแอปพลิเคชันคอนโซล C# หรือการบริการเว็บ หรือการสร้างไคลเอนต์ javascript/TypeScript

ตัวอย่างแอปพลิเคชันไคลเอนต์ C#:
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

หลังจากที่คุณได้ดึงโทเคนการเข้าถึงแล้ว คุณจะผ่านโทเคนในส่วนหัวของการตรวจสอบเป็นโทเคนผู้ถือสิทธิ์โดยมีคำขอแต่ละรายการที่คุณจะส่งไปยัง API ข้อมูลดังที่อธิบายไว้ข้างต้น


[!INCLUDE[footer-include](../includes/footer-banner.md)]