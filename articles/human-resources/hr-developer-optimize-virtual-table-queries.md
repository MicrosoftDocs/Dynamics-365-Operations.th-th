---
title: เพิ่มประสิทธิภาพการสอบถามตารางเสมือน Dataverse
description: เพิ่มประสิทธิภาพและแก้ไขปัญหาประสิทธิภาพของการสอบถามตารางเสมือน Dataverse
author: andreabichsel
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-04-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 66fb9f2b50079b5eb4eb16da17b8a473d687d354
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054919"
---
# <a name="optimize-dataverse-virtual-table-queries"></a><span data-ttu-id="de920-103">เพิ่มประสิทธิภาพการสอบถามตารางเสมือน Dataverse</span><span class="sxs-lookup"><span data-stu-id="de920-103">Optimize Dataverse virtual table queries</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a><span data-ttu-id="de920-104">ออก</span><span class="sxs-lookup"><span data-stu-id="de920-104">Issue</span></span>

### <a name="overview"></a><span data-ttu-id="de920-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="de920-105">Overview</span></span>

<span data-ttu-id="de920-106">เมื่อใช้ตารางเสมือน Dataverse เพื่อพัฒนาการรวมและการเชื่อมต่อข้อมูลอื่น ๆ ด้วย Dynamics 365 Human Resources คุณสามารถพบปัญหาเกี่ยวกับประสิทธิภาพการสอบถามกับตารางเสมือนได้</span><span class="sxs-lookup"><span data-stu-id="de920-106">When using Dataverse virtual tables to develop integrations and other data connections with Dynamics 365 Human Resources, you can experience performance issues with queries against the virtual tables.</span></span> <span data-ttu-id="de920-107">การปฏิบัติการสอบถามแบบช้าอาจเกิดขึ้นระหว่างไคลเอนต์หรืออินเทอร์เฟสต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="de920-107">The slow query execution can occur across various clients or interfaces.</span></span> <span data-ttu-id="de920-108">ตัวอย่างเช่น คุณอาจประสบกับปัญหาในสถานการณ์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="de920-108">For example, you may experience the issue in the following circumstances:</span></span>

- <span data-ttu-id="de920-109">เมื่อสอบถามตารางเสมือนผ่าน API ของเว็บ Dataverse</span><span class="sxs-lookup"><span data-stu-id="de920-109">When querying a virtual table through the Dataverse Web API</span></span>
- <span data-ttu-id="de920-110">เมื่อสร้าง Power App กับตารางเสมือน</span><span class="sxs-lookup"><span data-stu-id="de920-110">When creating a Power App against a virtual table</span></span>
- <span data-ttu-id="de920-111">เมื่อสร้างรายงาน Power BI ในตารางเสมือน</span><span class="sxs-lookup"><span data-stu-id="de920-111">When building a Power BI report on a virtual table</span></span>

<span data-ttu-id="de920-112">อินเทอร์เฟสเหล่านี้ทั้งหมดอาจมีปัญหาด้านประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="de920-112">All these interfaces have the potential to surface the performance issue.</span></span>

<span data-ttu-id="de920-113">สาเหตุหนึ่งของประสิทธิภาพการทำงานช้ากับตารางเสมือน Dataverse ของทรัพยากรบุคคลคือ คอลัมน์คีย์นอกของตารางเสมือนที่เกี่ยวข้องกับ [คุณสมบัติการนําทาง](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties) ของตาราง</span><span class="sxs-lookup"><span data-stu-id="de920-113">One cause of slow performance with Dataverse virtual tables for Human Resources is the foreign key columns of the virtual table related to the table's [navigation properties](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties).</span></span> <span data-ttu-id="de920-114">เมื่อสร้างคุณสมบัติการนําทางให้กับตารางเสมือน คอลัมน์คีย์นอกจะถูกเพิ่มเข้าในตารางโดยอัตโนมัติเพื่อแสดงค่าของคีย์ของคอลัมน์คีย์ของตารางเสมือนที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="de920-114">When navigation properties are created for a virtual table, a foreign key column is automatically added to the table to represent the value of the key for the related virtual table's key column.</span></span> <span data-ttu-id="de920-115">ตัวอย่างเช่น คอลัมน์ **_mshr_fk_person_id_value** จะถูกเพิ่มเข้าในเอนทิตี **mshr_hcmworkerbaseentity** กับคุณสมบัติคีย์นอกจากเอนทิตี **mshr_dirpersonentity**</span><span class="sxs-lookup"><span data-stu-id="de920-115">For example, the **_mshr_fk_person_id_value** column is added to the **mshr_hcmworkerbaseentity** entity with the foreign key property from the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="de920-116">เนื่องจากวิธีที่เก็บรักษาค่าสำหรับคีย์นอกเหล่านี้ในตารางเสมือน การดึงข้อมูลค่าอาจมีผลกระทบในทางลบต่อประสิทธิภาพของการสอบถามกับตารางเสมือน</span><span class="sxs-lookup"><span data-stu-id="de920-116">Because of how the values for these foreign key columns are maintained in a table, fetching the values can have a negative impact on the performance of a query against the virtual table.</span></span>

### <a name="potential-symptoms"></a><span data-ttu-id="de920-117">อาการที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="de920-117">Potential symptoms</span></span>

<span data-ttu-id="de920-118">ตัวอย่างที่คุณอาจเห็นผลกระทบนี้อยู่ในการสอบถามเกี่ยวกับผู้ปฏิบัติงาน (**mshr_hcmworkerentity**) หรือเอนทิตีผู้ปฏิบัติงานพื้นฐาน (**mshr_hcmworkerbaseentity**)</span><span class="sxs-lookup"><span data-stu-id="de920-118">An example where you may see this impact is in queries against the Worker (**mshr_hcmworkerentity**) or Base worker (**mshr_hcmworkerbaseentity**) entity.</span></span> <span data-ttu-id="de920-119">คุณอาจเห็นตัวรายการปัญหาประสิทธิภาพในสองสามวิธีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="de920-119">You may see the performance issue manifest itself in a few different ways:</span></span>

- <span data-ttu-id="de920-120">**การดําเนินการสอบถามช้า**: การสอบถามกับตารางเสมือนอาจส่งคืนผลลัพธ์ที่คาดไว้ แต่ใช้เวลานานกว่าที่คาดไว้ในการดําเนินการการสอบถามให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="de920-120">**Slow query execution**: The query against the virtual table may return the expected results, but take longer than expected to complete execution of the query.</span></span>
- <span data-ttu-id="de920-121">**การหมดเวลาของการสอบถาม**: การสอบถามอาจหมดเวลาและส่งคืนข้อผิดพลาดต่อไปนี้: "ได้รับโทเคนเพื่อเรียก Finance and Operations แต่ Finance and Operations ส่งคืนข้อผิดพลาดชนิด InternalServerError"</span><span class="sxs-lookup"><span data-stu-id="de920-121">**Query timeout**: The query may time out and return the following error: "A token was obtained to call Finance and Operations, but Finance and Operations returned an error of type InternalServerError."</span></span>
- <span data-ttu-id="de920-122">**ข้อผิดพลาดที่ไม่คาดคิด**: การสอบถามอาจส่งคืนชนิดข้อผิดพลาด 400 พร้อมด้วยข้อความต่อไปนี้: "เกิดข้อผิดพลาดที่ไม่คาดคิด"</span><span class="sxs-lookup"><span data-stu-id="de920-122">**Unexpected error**: The query may return an error type 400 with the following message: "An unexpected error occurred."</span></span>

  ![ชนิดข้อผิดพลาด 400 บน HcmWorkerBaseEntity](./media/HcmWorkerBaseEntityErrorType400.png)

- <span data-ttu-id="de920-124">**การควบคุมปริมาณ**: การสอบถามอาจใช้ทรัพยากรเซิร์ฟเวอร์มากเกินไปและอยู่ภายใต้การควบคุมปริมาณ</span><span class="sxs-lookup"><span data-stu-id="de920-124">**Throttling**: The query may overuse server resources, and become subject to throttling.</span></span> <span data-ttu-id="de920-125">ในกรณีนี้ การสอบถามจะส่งคืนข้อผิดพลาดต่อไปนี้: "ได้รับโทเคนเพื่อเรียก Finance and Operations แต่ Finance and Operations ส่งคืนข้อผิดพลาดชนิด 429"</span><span class="sxs-lookup"><span data-stu-id="de920-125">In this case, the query returns the following error: "A token was obtained to call Finance and Operations, but Finance and Operations returned an error of type 429."</span></span> <span data-ttu-id="de920-126">หากต้องการข้อมูลเพิ่มเติมเกี่ยวกับการควบคุมปริมาณในทรัพยากรบุคคล โปรดดูที่ [คำถามที่ถามบ่อยเกี่ยวกับการควบคุมปริมาณ](./hr-admin-integration-throttling-faq.md)</span><span class="sxs-lookup"><span data-stu-id="de920-126">For more information in throttling in Human Resources, see [Throttling FAQ](./hr-admin-integration-throttling-faq.md).</span></span>

  ![ชนิดข้อผิดพลาด 429 บน HcmWorkerBaseEntity](./media/HcmWorkerBaseEntityErrorType429.png)

## <a name="resolution"></a><span data-ttu-id="de920-128">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="de920-128">Resolution</span></span>

### <a name="limit-the-number-of-columns-included-in-your-data-query"></a><span data-ttu-id="de920-129">การจํากัดจํานวนคอลัมน์ที่รวมอยู่ในการสอบถามข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="de920-129">Limit the number of columns included in your data query</span></span>

<span data-ttu-id="de920-130">ด้วยตารางเสมือน วิธีการใดตารางหนึ่งที่มีความเป็นไปได้มากที่สุดในการปรับปรุงประสิทธิภาพของการสอบถาม คือจํากัดจํานวนคอลัมน์ที่เลือกในการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="de920-130">With virtual tables, one of the methods with the greatest potential to improve query performance is to limit the number of columns selected in the query.</span></span> <span data-ttu-id="de920-131">แนวทางทั่วไปสําหรับการเพิ่มประสิทธิภาพประสิทธิภาพของการสอบถาม คือจํากัดคอลัมน์ที่ส่งคืนในการสอบถามของคุณไปยังเฉพาะคุณสมบัติที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="de920-131">The general guidance for optimizing query performance is to limit the columns returned in your query to only those properties that you need.</span></span> <span data-ttu-id="de920-132">โดยเฉพาะอย่างยิ่งกับคอลัมน์คีย์นอกในตารางเสมือน</span><span class="sxs-lookup"><span data-stu-id="de920-132">This is particularly true with the foreign key columns on virtual tables.</span></span> <span data-ttu-id="de920-133">ถ้าคุณไม่ต้องการค่าในคอลัมน์คีย์นอกเพื่อการรวมหรือรายงานของคุณ ให้จัดโครงสร้างการสอบถามเพื่อเลือกเฉพาะคอลัมน์ที่คุณต้องการ โดยไม่รวมคอลัมน์คีย์นอก</span><span class="sxs-lookup"><span data-stu-id="de920-133">If you don't need the values in the foreign key columns for your integration or report, then structure the query to select only the columns you need, excluding the foreign key columns.</span></span>

#### <a name="selecting-columns-in-an-odata-query"></a><span data-ttu-id="de920-134">การเลือกคอลัมน์ในการสอบถาม OData</span><span class="sxs-lookup"><span data-stu-id="de920-134">Selecting columns in an OData query</span></span>

<span data-ttu-id="de920-135">เมื่อสอบถามตารางเสมือนผ่าน API ของเว็บ Dataverse คุณสามารถจํากัดจํานวนของคอลัมน์ที่รวมอยู่ในการสอบถามได้โดยใช้ตัวเลือกการสอบถามระบบ **$select** และกําหนดคอลัมน์ที่คุณต้องการส่งคืนผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="de920-135">When querying a virtual table through the Dataverse Web API, you can limit the number of columns included in the query by using the **$select** system query option, and define the columns for which you need results returned.</span></span> <span data-ttu-id="de920-136">เพื่อเพิ่มประสิทธิภาพให้สูงสุด แยกคอลัมน์คีย์นอก (คอลัมน์ที่มีคำนำหน้า **_mshr_FK_**) จากการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="de920-136">To maximize performance, exclude foreign key columns (those with the **_mshr_FK_** prefix) from the query.</span></span>

<span data-ttu-id="de920-137">ตัวอย่างเช่น การสอบถามต่อไปนี้เทียบกับเอนทิตี **mshr_hcmworkerbaseentity** จะรวมเฉพาะคอลัมน์ที่รวมอยู่ในอนุประโยคตัวเลือกการสอบถาม **$select** โดยไม่รวมค่าคีย์นอก</span><span class="sxs-lookup"><span data-stu-id="de920-137">For example, the following query against the **mshr_hcmworkerbaseentity** entity will include only the columns included in the **$select** query option clause, excluding foreign key values.</span></span> <span data-ttu-id="de920-138">สิ่งนี้จะให้การปรับปรุงประสิทธิภาพที่สําคัญเหนือกว่าการสอบถามที่มีคอลัมน์ตารางทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="de920-138">This provides significant improvements in performance over a query that includes all table columns.</span></span>

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas, mshr_professionaltitle, mshr_nativelanguageid, mshr_disabledverificationdate, mshr_personalsuffix, mshr_lastnameprefix, mshr_personbirthcity, mshr_personaltitle, mshr_phoneticlastname, mshr_namesequencedisplayas, mshr_personbirthcountryregion, mshr_isdisabled, mshr_birthdate, mshr_professionalsuffix, mshr_isfulltimestudent, mshr_education, mshr_namealias, mshr_phoneticmiddlename, mshr_personnelnumber, mshr_hcmworkerbaseentityid, mshr_motherbirthcountryregion, mshr_fatherbirthcountryregion, mshr_lastname, mshr_languageid, mshr_partytype, mshr_ethnicoriginid, mshr_citizenshipcountryregion HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

<span data-ttu-id="de920-139">ข้อแนะนําในการจํากัดจํานวนคอลัมน์ที่เลือกยังใช้เมื่อใช้ตัวเลือกการสอบถาม **$expand** เพื่อขยายการสอบถามไปยังตารางเสมือนที่เกี่ยวข้องผ่านคุณสมบัติการนําทาง</span><span class="sxs-lookup"><span data-stu-id="de920-139">The recommendation to limit the number of columns selected also applies when using the **$expand** query option to expand the query to related virtual tables through navigation properties.</span></span> <span data-ttu-id="de920-140">ตัวอย่างเช่น การสอบถามต่อไปนี้รวมคอลัมน์จากเอนทิตี **mshr_hcmworkerbaseentity** ที่มีคอลัมน์ขยายจากเอนทิตี **mshr_dirpersonentity**</span><span class="sxs-lookup"><span data-stu-id="de920-140">For example, the following query includes columns from the **mshr_hcmworkerbaseentity** entity with expanded columns from the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="de920-141">โปรดทราบว่าตัวเลือกการสอบถาม **$select** จะถูกรวมไว้ในอนุประโยคการสอบถาม **$expand** ด้วย</span><span class="sxs-lookup"><span data-stu-id="de920-141">Note that the **$select** query option is also included in the **$expand** query option clause.</span></span>

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas&$expand=mshr_FK_Person_id($select=mshr_addressstreet, mshr_addresscity, mshr_addressstate, mshr_addresszipcode) HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

<span data-ttu-id="de920-142">เมื่อใช้วิธีการดึงข้อมูลนี้โดยใช้ตัวเลือกการสอบถาม **$select** ในอนุประโยคตัวเลือกการสอบถาม **$expand** คุณจะเห็นการปรับปรุงประสิทธิภาพการนําทางมากขึ้นเมื่อคุณสมบัติการนําทางระหว่างเอนทิตีเป็นความสัมพันธ์แบบกลุ่มต่อหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="de920-142">When using this method of retrieving data with the **$select** query option in the **$expand** query option clause, you will typically see greater performance improvements when the navigation property between the entities is a many-to-one relationship.</span></span> <span data-ttu-id="de920-143">คุณอาจไม่เห็นการลดลงเดียวกันในเวลาการปฏิบัติการของการสอบถามเมื่อขยายความสัมพันธ์แบบหนึ่งต่อกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="de920-143">You may not see the same decrease in query execution time when expanding a one-to-many relationship.</span></span> <span data-ttu-id="de920-144">หากต้องการข้อมูลเพิ่มเติมเกี่ยวกับนิยามความสัมพันธ์สำหรับตารางเสมือน Dataverse โปรดดูที่ [ความสัมพันธ์ของตาราง](/powerapps/maker/data-platform/create-edit-entity-relationships)</span><span class="sxs-lookup"><span data-stu-id="de920-144">For more information on relationship definition for Dataverse virtual tables, see [Table relationships](/powerapps/maker/data-platform/create-edit-entity-relationships).</span></span>

<span data-ttu-id="de920-145">หากต้องการข้อมูลเพิ่มเติมเกี่ยวกับการใช้ตัวเลือกการสอบถามของระบบ **$select** และ **$expand** ใน API ของเว็บ โปรดดูที่ [ดึงข้อมูลเรกคอร์ดเอนทิตี Dataverse ที่เกี่ยวข้องกับการสอบถาม](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query)</span><span class="sxs-lookup"><span data-stu-id="de920-145">For more information on using the **$select** and **$expand** system query options in the Dataverse Web API, see [Retrieve related entity records with a query](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query).</span></span>

#### <a name="selecting-columns-in-power-bi"></a><span data-ttu-id="de920-146">การเลือกคอลัมน์ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="de920-146">Selecting columns in Power BI</span></span>

<span data-ttu-id="de920-147">หากคุณประสบการบ่งชี้ใด ๆ ที่กล่าวมาดังกล่าวเกี่ยวกับประสิทธิภาพการการปฏิบัติงานที่ช้าเมื่อสร้างรายงาน Power BI กับตารางเสมือน Dataverse คุณสามารถปรับปรุงประสิทธิภาพการงานได้ ด้วยการไม่รวมคอลัมน์คีย์นอกจากคอลัมน์ที่เลือกจากตารางของรายงาน</span><span class="sxs-lookup"><span data-stu-id="de920-147">If you experience any of the aforementioned indications of slow performance when building a Power BI report against a Dataverse virtual table, you can improve the performance by excluding foreign key columns from the columns selected from the table for the report.</span></span> <span data-ttu-id="de920-148">ตัวอย่างเช่น ถ้าคุณจะใช้ Power BI Desktop สร้างรายงานโดยเทียบกับเอนทิตี **mshr_hcmworkerbaseentity** นี้ คุณสามารถใช้ขั้นตอนต่อไปนี้เพื่อเลือกคอลัมน์ที่คุณต้องการรวมในการสอบถามของรายงาน</span><span class="sxs-lookup"><span data-stu-id="de920-148">For example, if you are using Power BI Desktop to create a report against the **mshr_hcmworkerbaseentity** entity, you can use the following steps to select the columns you want included in the report query.</span></span>

1. <span data-ttu-id="de920-149">ใน Power BI Desktop ให้เลือก **เพิ่มเติม...** จากรายการแบบหล่นลง **รับข้อมูล** บน Ribbon การดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="de920-149">In Power BI Desktop, select **More...** from the **Get data** drop-down list on the action ribbon.</span></span>
2. <span data-ttu-id="de920-150">ในหน้าต่าง **รับข้อมูล** ป้อน **Common Data Service** ในกล่องค้นหา เลือกตัวเชื่อมต่อ **Common Data Service** และเลือก **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="de920-150">In the **Get Data** window, enter **Common Data Service** in the search box, select the **Common Data Service** connector, and select **Connect**.</span></span>
3. <span data-ttu-id="de920-151">ในฟิลด์ **Url เซิร์ฟเวอร์** ของหน้าต่าง Common Data Service ให้ป้อน URI ขององค์กรให้กับสภาพแวดล้อม Dataverse ของคุณ และเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="de920-151">In the **Server Url** field of the Common Data Service window, enter the organization URI for your Dataverse environment, and select **OK**.</span></span>
  
   ![ป้อน URI สำหรับสภาพแวดล้อม Dataverse ของคุณ](./media/PowerBIDataverseURLSetup.png)
  
4. <span data-ttu-id="de920-153">ในหน้าต่างตัวนําทาง ให้ขยายโหนด **เอนทิตี**</span><span class="sxs-lookup"><span data-stu-id="de920-153">In the Navigator window, expand the **Entities** node.</span></span>
5. <span data-ttu-id="de920-154">ในกล่องค้นหา ให้ป้อน **mshr_hcmworkerbaseentity** และเลือกเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="de920-154">In the search box, enter **mshr_hcmworkerbaseentity**, and select the entity.</span></span>
6. <span data-ttu-id="de920-155">เลือก **แปลงข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="de920-155">Select **Transform Data**.</span></span>
7. <span data-ttu-id="de920-156">ในหน้าต่างตัวแก้ไข Power Query ให้เลือก **เครื่องมือแก้ไขขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="de920-156">In the Power Query Editor window, select **Advanced Editor**.</span></span>
8. <span data-ttu-id="de920-157">ในหน้าต่างโปรแกรม **เครื่องมือแก้ไขขั้นสูง** ให้อัปเดตการสอบถามให้มีลักษณะเป็นด้านล่าง เพิ่มหรือลบคอลัมน์ใด ๆ ไปยังแถวลำดับที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="de920-157">In the **Advanced Editor** window, update the query to look like the below, adding or removing any columns to the array as needed.</span></span>

   ```
   let
     Source = Cds.Entities("[Your Organization URI]", [ReorderColumns=null, UseFormattedValue=null]),
     entities = Source{[Group="entities"]}[Data],
     mshr_hcmworkerbaseentities = entities{[EntitySetName="mshr_hcmworkerbaseentities"]}[Data],
     selectedWorkerBaseEntityColumns=Table.SelectColumns(mshr_hcmworkerbaseentities,{"mshr_name","mshr_partynumber", "mshr_professionaltitle","mshr_birthdate"})
   in
     selectedWorkerBaseEntityColumns
   ```
   ![อัปเดตการสอบถามในฟิลด์เครื่องมือแก้ไขขั้นสูงสำหรับตัวแก้ไข Power Query](./media/HcmWorkerBaseEntityPowerQueryEditor.png)

9. <span data-ttu-id="de920-159">เลือก **เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="de920-159">Select **Done**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="de920-160">ถ้าคุณได้รับข้อผิดพลาดชนิด 429 จากการสอบถามก่อนที่จะอัปเดต คุณอาจต้องรอรอบระยะเวลาการลองส่งใหม่ก่อนที่จะรีเฟรชการสอบถามเพื่อให้การการสอบถามเสร็จสมบูรณ์อย่างต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="de920-160">If you previously received an error of type 429 from the query prior to updating, you may need to wait for the retry period prior to refreshing the query for it to complete successully.</span></span>

10. <span data-ttu-id="de920-161">คลิก **ปิด & นำไปใช้** บน Ribbon การดำเนินการตัวแก้ไข Power Query</span><span class="sxs-lookup"><span data-stu-id="de920-161">Click **Close & Apply** on the Power Query Editor action ribbon.</span></span>

<span data-ttu-id="de920-162">จากนั้นคุณสามารถเริ่มต้นสร้างรายงาน Power BI ของคุณโดยเทียบกับคอลัมน์ที่เลือกจากตารางเสมือนได้</span><span class="sxs-lookup"><span data-stu-id="de920-162">You're then able to begin building your Power BI report against the columns selected from the virtual table.</span></span>

#### <a name="selecting-columns-in-power-apps"></a><span data-ttu-id="de920-163">การเลือกคอลัมน์ใน Power Apps</span><span class="sxs-lookup"><span data-stu-id="de920-163">Selecting columns in Power Apps</span></span>

<span data-ttu-id="de920-164">คล้ายกับการสอบถาม API ของเว็บ Dataverse และ Power BI คุณสามารถปรับปรุงประสิทธิภาพการสอบถามสำหรับ Power Apps ให้ดีขึ้นได้ตามตารางเสมือน Dataverse โดยไม่รวมคอลัมน์ของตารางที่เกี่ยวข้องจากแอปของคุณ</span><span class="sxs-lookup"><span data-stu-id="de920-164">Similar to Dataverse Web API queries and Power BI, you can improve query performance for Power Apps based on Dataverse virtual tables by excluding columns of related tables from your app.</span></span> <span data-ttu-id="de920-165">ถ้ารวมคอลัมน์ใด ๆ จากตารางที่เกี่ยวข้องบนหน้า URL คำขอที่สร้างขึ้นเพื่อดึงข้อมูลจะรวมคุณสมบัติคีย์นอกของตารางที่เกี่ยวข้องด้วย</span><span class="sxs-lookup"><span data-stu-id="de920-165">If any columns from a related table have been included on a page, then the request URL constructed to fetch the data will include foreign key properties of the related table.</span></span> <span data-ttu-id="de920-166">ในตัวอย่างของ [การเลือกคอลัมน์ใน OData Query](#selecting-columns-in-power-apps) ข้างต้น จะลดประสิทธิภาพโดยทําให้การค้นหาข้อมูลเพิ่มเติมลดลง</span><span class="sxs-lookup"><span data-stu-id="de920-166">This, as in the examples of [Selecting columns in an OData Query](#selecting-columns-in-power-apps) above, reduces performance by causing additional data lookups.</span></span>

<span data-ttu-id="de920-167">เมื่อต้องการแก้ไขปัญหานี้ คุณสามารถตรวจสอบความถูกต้องว่าไม่มีฟิลด์ข้อมูลจากตารางที่เกี่ยวข้องรวมอยู่ในฟอร์มข้อมูลใด ๆ ของ Power App ของคุณ</span><span class="sxs-lookup"><span data-stu-id="de920-167">To work around this, you can validate that no data fields from related tables have been included on any data form of your Power App.</span></span>

1. <span data-ttu-id="de920-168">ในบานหน้าต่างมุมมองแผนภูมิ เลือกฟอร์มข้อมูลหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="de920-168">In the Tree view pane, select the data form for the screen.</span></span>
2. <span data-ttu-id="de920-169">ในบานหน้าต่าง **คุณสมบัติ** ให้เลือก **แก้ไข** บนคุณสมบัติ **ฟิลด์**</span><span class="sxs-lookup"><span data-stu-id="de920-169">In the **Properties** pane, select **Edit** on the **Fields** property.</span></span>
3. <span data-ttu-id="de920-170">ในบานหน้าต่าง **ข้อมูล** ให้ตรวจสอบว่าไม่มีฟิลด์ที่เลือกใดเป็นฟิลด์ของตารางเสมือนของแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="de920-170">In the **Data** pane, verify that none of the selected fields are fields of the virtual table of the data source.</span></span>

<span data-ttu-id="de920-171">ตัวอย่างเช่น ถ้าฟิลด์ใดฟิลด์หนึ่งที่รวมอยู่ในหน้าแอปอ้างอิงอีกตารางหนึ่ง เช่น **ThisItem.Worker.Name** โดยที่ **ผู้ปฏิบัติงาน** เป็นตารางที่เกี่ยวข้อง อาจมีประสิทธิภาพการลดลงในการดึงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="de920-171">For example, if one of the data fields included on a page in the app references another table, such as **ThisItem.Worker.Name**, where **Worker** is the related table, there is a potential for reduced performance in fetching the data.</span></span>

<span data-ttu-id="de920-172">คุณสามารถใช้ [Power Apps Monitor](/powerapps/maker/monitor-overview) เพื่อให้แน่ใจว่าเฉพาะคอลัมน์ที่คุณต้องการรวมอยู่ในการสอบถามเพื่อรับข้อมูลใน Power App</span><span class="sxs-lookup"><span data-stu-id="de920-172">You can use the [Power Apps Monitor](/powerapps/maker/monitor-overview) to ensure that only the columns you need are being included in the query to get the data for the Power App.</span></span> <span data-ttu-id="de920-173">คุณสามารถดู URL ที่สร้างไว้ให้กับการดําเนินงาน getRows เพื่อให้แน่ใจว่าคอลัมน์ที่คุณเลือกไว้เพื่อให้แอปของคุณมีประสิทธิภาพสูงสุดในการดึงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="de920-173">You can view the URL constructed for the getRows operation to ensure the columns you have selected for your app will be optimal for retrieving the data.</span></span>

![ใช้ Power Apps Monitor เพื่อวิเคราะห์การดําเนินงาน getData](./media/HcmWorkerBaseEntityPowerAppsMonitor.png)

### <a name="filtering-the-data-query"></a><span data-ttu-id="de920-175">การกรองการสอบถามข้อมูล</span><span class="sxs-lookup"><span data-stu-id="de920-175">Filtering the data query</span></span>

<span data-ttu-id="de920-176">วิธีการอื่นในการปรับปรุงประสิทธิภาพการดําเนินการสอบถามคือจํากัดจํานวนของเรกคอร์ดที่ส่งคืนในผลลัพธ์ของการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="de920-176">Another method for improving query execution performance is to limit the number of records returned in the query results.</span></span> <span data-ttu-id="de920-177">คุณสามารถดําเนินการนี้โดยการกรองผลลัพธ์เพื่อให้แน่ใจว่าคุณจะได้รับเรกคอร์ดที่คุณต้องการเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="de920-177">You can do this by filtering the results to ensure that you are only receiving the records you need.</span></span>

<span data-ttu-id="de920-178">ดู [ผลลัพธ์ตัวกรอง](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results) สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการกรองข้อมูลการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="de920-178">See [Filter results](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results) for more information on filtering query data.</span></span>

### <a name="limiting-the-page-size-of-the-query"></a><span data-ttu-id="de920-179">การจํากัดขนาดหน้าของการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="de920-179">Limiting the page size of the query</span></span>

<span data-ttu-id="de920-180">ถ้าคุณใช้งานชุดข้อมูลขนาดใหญ่ คุณสามารถแบ่งผลลัพธ์ของการสอบถามออกเป็นหน้าหลายหน้าได้โดยการเพิ่มหัวข้อกำหนดลักษณะ `odata.maxpagesize` ที่การสอบถามข้อมูล</span><span class="sxs-lookup"><span data-stu-id="de920-180">If you're working with large data sets, you can divide query results into multiple pages by adding the `odata.maxpagesize` preference header to data queries.</span></span>

<span data-ttu-id="de920-181">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการจัดหน้า ให้ดูที่ [ระบุจำนวนของเอนทิตีที่จะส่งคืนในหน้า](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page)</span><span class="sxs-lookup"><span data-stu-id="de920-181">For more information on paging, see [Specify the number of entities to return in a page](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page).</span></span>

## <a name="see-also"></a><span data-ttu-id="de920-182">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="de920-182">See also</span></span>

- [<span data-ttu-id="de920-183">ตั้งค่าคอนฟิกตารางเสมือน Dataverse</span><span class="sxs-lookup"><span data-stu-id="de920-183">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)
- [<span data-ttu-id="de920-184">คำถามที่ถามบ่อยเกี่ยวกับตารางเสมือน Human Resources</span><span class="sxs-lookup"><span data-stu-id="de920-184">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)
- [<span data-ttu-id="de920-185">คำถามที่ถามบ่อยเกี่ยวกับการควบคุมปริมาณ</span><span class="sxs-lookup"><span data-stu-id="de920-185">Throttling FAQ</span></span>](./hr-admin-integration-throttling-faq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]