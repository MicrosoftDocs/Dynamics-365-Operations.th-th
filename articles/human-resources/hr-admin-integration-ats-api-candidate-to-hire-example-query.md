---
title: ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน
description: หัวข้อนี้แสดงตัวอย่างการสอบถามสำหรับเอนทิตี้ผู้สมัครที่จะจ้างใน Dynamics 365 Human Resources
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 963e12e9114664a995b92ffe22063c14f904da35
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125772"
---
# <a name="example-query-for-candidate-to-hire"></a>ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน

หัวข้อนี้แสดงตัวอย่างการสอบถามสำหรับเอนทิตี้ผู้สมัครที่จะจ้างใน Dynamics 365 Human Resources

หัวข้อนี้แสดงตัวอย่างตัวอย่างการสาธิตวิธีการใช้ *การแทรกแบบลึก* เพื่อสร้างรายละเอียดทั้งหมดของบันทึกผู้สมัครในการดำเนินงาน API เดียว สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการแทรกแบบลึกให้ดูที่ [สร้างบันทึกเอนทิตี้ที่เกี่ยวข้องในการดําเนินงานเดียว](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-entity-web-api#create-related-entity-records-in-one-operation)

เอนทิตี **mshr_hcmcandidatetohireentity** ที่ไม่ซ้ำกันเนื่องจากความสัมพันธ์กับเอนทิตี้ **mshr_dirpersonentity** คุณสมบัติหลายอย่างบน **mshr_hcmcandidatetohireentity** (ตัวอย่างเช่น **mshr_firstname** **mshr_lastname** และ **mshr_birthdate**) ได้รับมาจากบันทึก **mshr_dirpersonentity** ถ้าคุณลงรายการบัญชีบันทึกผู้สมัครใหม่ไปยัง **mshr_hcmcandidatetohireentity** โดยไม่ใช้การแทรกแบบลึก คุณสามารถกําหนดค่าสำหรับคุณสมบัติเหล่านี้โดยตรงบนบันทึก **mshr_hcmcandidatetohireentity** บันทึก **mshr_dirpersonentity** ที่เกี่ยวข้องจะถูกสร้างขึ้นอย่างชัดเจนกับค่าที่กําหนดไว้สำหรับคุณสมบัติ จากนั้นคุณสามารถสร้างบันทึกเอนทิตี้ที่เกี่ยวข้องอื่นๆ (เช่น ทักษะหรือการศึกษา) เป็นการเรียก API ที่แยกต่างหากได้

อย่างไรก็ตาม ถ้าคุณต้องการใช้การแทรกแบบลึกเพื่อสร้างเอนทิตี้ที่เกี่ยวข้องทั้งหมดในการดําเนินงานเดียว คุณสมบัติเฉพาะของเอนทิตี้ **mshr_dirpersonentity** ต้องถูกกำหนดในระดับที่ซ้อนกันของการดําเนินงาน

ตัวอย่างนี้แสดงวิธีการสร้างบันทึกผู้สมัคร บันทึกบุคคลที่เกี่ยวข้อง และทักษะและการศึกษาของบุคคลในระดับที่ซ้อนกันสามระดับ โดยใช้การแทรกแบบลึกในการดําเนินงาน API เดียว

> [!NOTE]
> ตัวอย่างจะไม่รวมคุณสมบัติทั้งหมดของแต่ละเอนทิตี้ API จะง่ายขึ้นสำหรับใช้เพื่อวัตถุประสงค์ในการสาธิต

**คำขอ**

```http

POST [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities
Content-Type: application/json; charset=utf-8
OData-MaxVersion: 4.0
OData-Version: 4.0
Accept: application/json

{
    "mshr_dataareaid": "usmf",
    "mshr_recruitingrequestid": "USMF-000141",
    "mshr_positionid": "000601",
    "mshr_iswillingtorelocate": 200000000,
    "mshr_availabilitydate": "2021-03-18",
    "mshr_comments": "Evelyn's experience is exactly what we need for this position.",
    "mshr_FK_Person_id":
        {
            "mshr_firstname": "Evelyn",
            "mshr_lastname": "Chambers",
            "mshr_namesequencedisplayas": "FirstMiddleLast",
            "mshr_FK_HcmPersonSkillEntity_Person":
            [
                {
                    "mshr_skillid": "CustFocus",
                    "mshr_ratingid": "Skills",
                    "mshr_levelid": "4",
                    "mshr_ratinglevelexaminer": "",
                    "mshr_leveltype": 200000000,
                    "mshr_yearsofexperience": 0,
                    "mshr_verified": 200000000,
                    "mshr_leveldate": "2013-01-01T00:00:00Z"
                },
                {
                    "mshr_skillid": "CashFlow",
                    "mshr_ratingid": "Skills",
                    "mshr_levelid": "4",
                    "mshr_ratinglevelexaminer": "",
                    "mshr_leveltype": 200000000,
                    "mshr_yearsofexperience": 0,
                    "mshr_verified": 200000000,
                    "mshr_leveldate": "2013-01-01T00:00:00Z"
                }
            ],
            "mshr_FK_HcmPersonEducationEntity_Person": [
                {
                    "mshr_creditbasis": 200000000,
                    "mshr_enddate": "2021-02-22T00:00:00Z",
                    "mshr_educationlevelid": "Bachelor",
                    "mshr_creditsearned": 0,
                    "mshr_startdate": "2017-02-21T00:00:00Z",
                    "mshr_creditscompleted": 0,
                    "mshr_educationinstitutionid": "Cottonwood Univ",
                    "mshr_educationdisciplineid": "Business Mgmt",
                    "mshr_durationunit": 200000000
                }              
            ]
        }
}
```

**การตอบสนอง**

```http

HTTP/1/1 204 No Content
OData-Version: 4.0
OData-EntityId: [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities(00000d2d-0000-0000-7317-005001000000)

```

## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนํา API การรวมระบบการติดตามผู้สมัคร](hr-admin-integration-ats-api-introduction.md)<br>
