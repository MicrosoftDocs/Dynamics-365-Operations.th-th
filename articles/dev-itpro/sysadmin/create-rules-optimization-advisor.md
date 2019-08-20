---
title: สร้างกฎสำหรับโปรแกรมช่วยแนะนำการปรับให้เหมาะสม
description: หัวข้อนี้อธิบายวิธีการเพิ่มกฎใหม่ในโปรแกรมช่วยแนะนำการปรับให้เหมาะสม
author: roxanadiaconu
manager: AnnBe
ms.date: 02/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SelfHealingWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: roxanad
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 27066cd860d78743d5ae7c851876eb62fe019245
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851432"
---
# <a name="create-rules-for-optimization-advisor"></a><span data-ttu-id="6decd-103">สร้างกฎสำหรับโปรแกรมช่วยแนะนำการปรับให้เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="6decd-103">Create rules for Optimization advisor</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6decd-104">หัวข้อนี้อธิบายวิธีการสร้างกฎใหม่สำหรับ **โปรแกรมช่วยแนะนำการปรับให้เหมาะสม**</span><span class="sxs-lookup"><span data-stu-id="6decd-104">This topic explains how to create new rules for **Optimization advisor**.</span></span> <span data-ttu-id="6decd-105">ตัวอย่างเช่น คุณสามารถสร้างกฎใหม่ที่ระบุกรณีของคำขอใบเสนอราคา (RFQ) ที่มีชื่อเรื่องแบบว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="6decd-105">For example, you can create a new rule that identifies which Request for Quotations (RFQ) cases have an empty title.</span></span> <span data-ttu-id="6decd-106">การใช้ชื่อในกรณีทำให้สามารถระบุและสามารถค้นหาได้ง่าย</span><span class="sxs-lookup"><span data-stu-id="6decd-106">Using titles on cases makes them easily identifiable and searchable.</span></span> <span data-ttu-id="6decd-107">ขณะที่ค่อนข้างอย่างง่าย ตัวอย่างนี้แสดงสิ่งที่สามารถทำได้ด้วยกฎการปรับให้เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="6decd-107">While quite simple, this example shows what can be achieved with optimization rules.</span></span> 

<span data-ttu-id="6decd-108">*กฎ* เป็นการตรวจสอบข้อมูลแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="6decd-108">A *rule* is a check on application data.</span></span> <span data-ttu-id="6decd-109">ถ้าเป็นไปตามเงื่อนไขที่กฎประเมิน จะมีการสร้างโอกาสในการเพิ่มประสิทธิภาพกระบวนการ หรือปรับปรุงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6decd-109">If the condition that the rule evaluates is met, opportunities to optimize processes or improve data are created.</span></span> <span data-ttu-id="6decd-110">โอกาสที่สามารถดำเนินการ และอีกทางหนึ่งคือ สามารถวัดผลกระทบของการดำเนินการได้</span><span class="sxs-lookup"><span data-stu-id="6decd-110">The opportunities can be acted upon and, optionally, the impact of the actions can be measured.</span></span> 

<span data-ttu-id="6decd-111">ในการสร้างกฎใหม่สำหรับ **โปรแกรมช่วยแนะนำการปรับให้เหมาะสม** เพิ่มคลาสใหม่ที่ขยายคลาสนามธรรม **SelfHealingRule** ใช้อินเทอร์เฟส **IDiagnosticsRule** และถูกตกแต่งโดยแอตทริบิวต์ **DiagnosticRule**</span><span class="sxs-lookup"><span data-stu-id="6decd-111">To create a new rule for the **Optimization advisor**, add a new class that extends the **SelfHealingRule** abstract class, implements the **IDiagnosticsRule** interface, and is decorated by the **DiagnosticRule** attribute.</span></span> <span data-ttu-id="6decd-112">คลาสต้องมีวิธีที่ถูกตกแต่งด้วยแอตทริบิวต์ **DiagnosticsRuleSubscription**</span><span class="sxs-lookup"><span data-stu-id="6decd-112">The class must also have a method decorated with the **DiagnosticsRuleSubscription** attribute.</span></span> <span data-ttu-id="6decd-113">ตามแบบแผน ซึ่งเสร็จสิ้นในวิธี **opportunityTitle** ซึ่งจะกล่าวถึงในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="6decd-113">By convention, that is done on the **opportunityTitle** method, which will be discussed later.</span></span> <span data-ttu-id="6decd-114">คลาสใหม่นี้สามารถถูกเพิ่มไปยังแบบจำลองที่กำหนดเองที่มีการขึ้นต่อกันในแบบจำลอง **SelfHealingRules** ได้</span><span class="sxs-lookup"><span data-stu-id="6decd-114">This new class can be added to a custom model with a dependency on the **SelfHealingRules** model.</span></span> <span data-ttu-id="6decd-115">ในตัวอย่างต่อไปนี้ กฎที่กำลังถูกใช้ เรียกว่า **RFQTitleSelfHealingRule**</span><span class="sxs-lookup"><span data-stu-id="6decd-115">In the following example, the rule being implemented is called **RFQTitleSelfHealingRule**.</span></span>

```
[DiagnosticsRule] 
public final class RFQTitleSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule 
{ 
… 
} 
```

<span data-ttu-id="6decd-116">คลาสนามธรรม **SelfHealingRule** มีวิธีการนามธรรมที่ต้องดำเนินการในคลาสที่สืบทอด</span><span class="sxs-lookup"><span data-stu-id="6decd-116">The **SelfHealingRule** abstract class has abstract methods that must be implemented in inheriting classes.</span></span> <span data-ttu-id="6decd-117">หลักคือ วิธี **ประเมิน** ซึ่งส่งกลับรายการของโอกาสที่ระบุโดยกฎ</span><span class="sxs-lookup"><span data-stu-id="6decd-117">The core is the **evaluate** method, which returns a list of the opportunities identified by the rule.</span></span> <span data-ttu-id="6decd-118">โอกาสสามารถเป็นต่อนิติบุคคล หรือสามารถนำไปใช้กับทั้งระบบได้</span><span class="sxs-lookup"><span data-stu-id="6decd-118">Opportunities can be per legal entity or can apply to the whole system.</span></span>

```
protected List evaluate() 
{ 
    List results = new List(Types::Record); 
    
    DataArea dataArea; 

    while select id from dataArea 
        where !dataArea.isVirtual 
    { 
        changecompany(dataArea.id) 
        { 
            container result = this.findRFQCasesWithEmptyTitle(); 

            if (conLen(result) > 0) 
            { 
                SelfHealingOpportunity opportunity = this.getOpportunityForCompany(dataArea.Id); 
                opportunity.EvaluationState = SelfHealingEvaluationState::Evaluated; 
                opportunity.Data = result; 
                opportunity.OpportunityDate = DateTimeUtil::utcNow(); 
                
                results.addEnd(opportunity); 
            } 
        } 
    } 
    
    return results; 
} 
```

<span data-ttu-id="6decd-119">วิธีการที่แสดงไว้ข้างบนวนผ่านบริษัทและเลือกกรณี RFQ ที่มีชื่อเรื่องแบบว่างเปล่าในวิธี **findRFQCasesWithEmptyTitle**</span><span class="sxs-lookup"><span data-stu-id="6decd-119">The method shown above loops over companies and selects RFQ cases with empty titles in the **findRFQCasesWithEmptyTitle** method.</span></span> <span data-ttu-id="6decd-120">ถ้ามีการพบกรณีดังกล่าวอย่างน้อยหนึ่งกรณี โอกาสทางการขายเฉพาะบริษัทจะถูกสร้างขึ้นด้วยวิธี **getOpportunityForCompany**</span><span class="sxs-lookup"><span data-stu-id="6decd-120">If at least one such case is found, then a company-specific opportunity is created with the **getOpportunityForCompany** method.</span></span> <span data-ttu-id="6decd-121">สังเกตว่า ฟิลด์ **ข้อมูล** ในตาราง **SelfHealingOpportunity** เป็นชนิด **คอนเทนเนอร์** และดังนั้นจึงสามารถประกอบด้วยข้อมูลที่เกี่ยวข้องกับตรรกะเฉพาะสำหรับกฎนี้</span><span class="sxs-lookup"><span data-stu-id="6decd-121">Notice that the field **Data** in the **SelfHealingOpportunity** table is of type **Container**, and can therefore contain any data relevant to the logic specific to this rule.</span></span> <span data-ttu-id="6decd-122">การตั้งค่า **OpportunityDate** ด้วยการประทับเวลาปัจจุบันจะลงทะเบียนเวลาของการประเมินล่าสุดของโอกาส</span><span class="sxs-lookup"><span data-stu-id="6decd-122">Setting **OpportunityDate** with the current timestamp registers the time of the latest evaluation of the opportunity.</span></span>  

<span data-ttu-id="6decd-123">โอกาสทางการขายอาจเป็นระหว่างบริษัทได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="6decd-123">Opportunities can also be cross-company.</span></span> <span data-ttu-id="6decd-124">ในกรณีนี้ ลูปที่ผ่านบริษัทไม่จำเป็น และต้องมีการสร้างโอกาสด้วยวิธี **getOpportunityAcrossCompanies**</span><span class="sxs-lookup"><span data-stu-id="6decd-124">In this case, the loop over companies is not necessary and the opportunity must be created with the **getOpportunityAcrossCompanies** method.</span></span> 

<span data-ttu-id="6decd-125">โค้ดต่อไปนี้แสดงวิธี **findRFQCasesWithEmptyTitle** ซึ่งส่งกลับรหัสของกรณี RFQ ที่มีชื่อที่ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="6decd-125">The following code shows the **findRFQCasesWithEmptyTitle** method, which returns the IDs of the RFQ cases that have empty titles.</span></span>

```
private container findRFQCasesWithEmptyTitle() 
{ 
    container result; 

    PurchRFQCaseTable rfqCase; 
    while select RFQCaseId from rfqCase 
        where rfqCase.Name == '' 
    { 
        result += rfqCase.RFQCaseId; 
    } 
    
    return result; 
} 
```

<span data-ttu-id="6decd-126">วิธีเพิ่มเติมที่ต้องถูกนำมาใช้คือ **opportunityTitle** และ **opportunityDetails**</span><span class="sxs-lookup"><span data-stu-id="6decd-126">Two more methods that must be implemented are **opportunityTitle** and **opportunityDetails**.</span></span> <span data-ttu-id="6decd-127">ค่าเดิมคืนค่าชื่อเรื่องแบบสั้นสำหรับโอกาส ค่าหลังส่งคืนคำอธิบายโดยละเอียดของโอกาสทางการขาย ซึ่งยังสามารถมีข้อมูลอยู่ได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="6decd-127">The former returns a short title for the opportunity, the latter returns a detailed description of the opportunity, which can also include data.</span></span>

<span data-ttu-id="6decd-128">ชื่อเรื่องที่ส่งคืนโดย **opportunityTitle** ปรากฏอยู่ภายใต้คอลัมน์ **โอกาสในการปรับให้เหมาะสม** ในพื้นที่ทำงาน **โปรแกรมช่วยแนะนำการปรับให้เหมาะสม**</span><span class="sxs-lookup"><span data-stu-id="6decd-128">The title returned by **opportunityTitle** appears under the **Optimization opportunity** column in the **Optimization advisor** workspace.</span></span> <span data-ttu-id="6decd-129">นอกจากนี้ยังปรากฏเป็นส่วนหัวของบานหน้าต่างด้านข้างที่แสดงข้อมูลเพิ่มเติมเกี่ยวกับโอกาสด้วย</span><span class="sxs-lookup"><span data-stu-id="6decd-129">It also appears as the header of the side pane showing more information about the opportunity.</span></span> <span data-ttu-id="6decd-130">ตามแบบแผน วิธีการนี้ถูกปรับปรุงด้วยแอตทริบิวต์ **DiagnosticRuleSubscription** ซึ่งใช้อาร์กิวเมนต์ดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6decd-130">By convention, this method is decorated with the **DiagnosticRuleSubscription** attribute, which takes the following arguments:</span></span> 

* <span data-ttu-id="6decd-131">**พื้นที่วินิจฉัย** – enum ของชนิด **DiagnosticArea** ที่อธิบายว่าพื้นที่ใดของแอพลิเคชันที่มีกฎอยู่ เช่น **DiagnosticArea::SCM**</span><span class="sxs-lookup"><span data-stu-id="6decd-131">**Diagnostic area** – An enum of type **DiagnosticArea** that describes what area of the application the rule belongs to, such as **DiagnosticArea::SCM**.</span></span> 

* <span data-ttu-id="6decd-132">**ชื่อกฎ** – สตริงที่มีชื่อกฎ</span><span class="sxs-lookup"><span data-stu-id="6decd-132">**Rule name** – A string with the rule name.</span></span> <span data-ttu-id="6decd-133">นี่จะปรากฏขึ้นภายใต้คอลัมน์ **ชื่อกฎ** ในแบบฟอร์ม **กฎการตรวจสอบความถูกต้องของการวิเคราะห์** (**DiagnosticsValidationRuleMaintain**)</span><span class="sxs-lookup"><span data-stu-id="6decd-133">This will appear under the **Rule name** column in the **Dianostics validation rule** form (**DiagnosticsValidationRuleMaintain**).</span></span> 

* <span data-ttu-id="6decd-134">**ความถี่ในการรัน** – enum ของชนิด **DiagnosticRunFrequency** ที่อธิบายความถี่ที่กฎควรถูกรัน เช่น **DiagnosticRunFrequency::รายวัน**</span><span class="sxs-lookup"><span data-stu-id="6decd-134">**Run frequency** – An enum of type **DiagnosticRunFrequency** that describes how often the rule should be run, such as **DiagnosticRunFrequency::Daily**.</span></span> 

* <span data-ttu-id="6decd-135">**คำอธิบายกฎ** – สตริงที่มีคำอธิบายโดยละเอียดมากขึ้นของกฎ</span><span class="sxs-lookup"><span data-stu-id="6decd-135">**Rule description** – A string with a more detailed description of the rule.</span></span> <span data-ttu-id="6decd-136">นี่จะปรากฏขึ้นภายใต้คอลัมน์ **คำอธิบายกฎ** ในแบบฟอร์ม **กฎการตรวจสอบความถูกต้องของการวิเคราะห์** (**DiagnosticsValidationRuleMaintain**)</span><span class="sxs-lookup"><span data-stu-id="6decd-136">This will appear under the **Rule description** column in the **Dianostics validation rule** form (**DiagnosticsValidationRuleMaintain**).</span></span> 

> [!NOTE]
> <span data-ttu-id="6decd-137">แอททริบิวต์ **DiagnosticRuleSubscription** จำเป็นสำหรับกฎในการทำงาน</span><span class="sxs-lookup"><span data-stu-id="6decd-137">The **DiagnosticRuleSubscription** attribute is required for the rule to work.</span></span> <span data-ttu-id="6decd-138">โดยทั่วไป จะมีการใช้ใน **opportunityTitle** แต่จะสามารถตกแต่งวิธีใดๆ ของคลาสได้</span><span class="sxs-lookup"><span data-stu-id="6decd-138">Typically, it is used on **opportunityTitle**, but it can decorate any method of the class.</span></span>

<span data-ttu-id="6decd-139">รายการต่อไปนี้เป็นการนำไปใช้แบบตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="6decd-139">The following is an example implementation.</span></span> <span data-ttu-id="6decd-140">มีการใช้สตริงการดิบสำหรับความเรียบง่าย แต่การใช้งานที่ถูกต้องต้องมีป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="6decd-140">Raw strings are used for simplicity, but a correct implementation requires labels.</span></span> 

```
[DiagnosticsRuleSubscription(DiagnosticsArea::SCM, 
                             'Assign titles to Request for Quotation cases', 
                             DiagnosticsRunFrequency::Daily,  
                             'This rule detects Requests for Quotation with empty titles.')] 
public str opportunityTitle() 
{ 
    return 'Assign titles to Request for Quotation cases'; 
} 
```

<span data-ttu-id="6decd-141">คำอธิบายที่ส่งคืนโดย **opportunityDetails** ปรากฏในบานหน้าต่างด้านข้างที่แสดงข้อมูลเพิ่มเติมเกี่ยวกับโอกาส</span><span class="sxs-lookup"><span data-stu-id="6decd-141">The description returned by **opportunityDetails** appears on the side pane showing more information about the opportunity.</span></span> <span data-ttu-id="6decd-142">นี่จะใช้อาร์กิวเมนต์ **SelfHealingOpportunity** ซึ่งก็คือฟิลด์ **ข้อมูล** ที่สามารถใช้เพื่อระบุรายละเอียดเพิ่มเติมเกี่ยวกับโอกาสได้</span><span class="sxs-lookup"><span data-stu-id="6decd-142">This takes the **SelfHealingOpportunity** argument, which is **Data** field that can be used to provide more details about the opportunity.</span></span> <span data-ttu-id="6decd-143">ในตัวอย่าง วิธีส่งคืนรหัสของกรณี RFQ ที่มีชื่อเรื่องแบบว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="6decd-143">In the example, the method returns the IDs of the RFQ cases with an empty title.</span></span> 

```
public str opportunityDetails(SelfHealingOpportunity _opportunity) 
{ 
    str details = ''; 
    container opportunityData = _opportunity.Data; 
    int affectedRFQCasesCount = conLen(opportunityData); 

    if (affectedRFQCasesCount != 0) 
    { 
        details = 'The following Request for Quotation cases have an empty title:\n'; 
        for (int i = 1; i <= affectedRFQCasesCount ; i++) 
        { 
            PurchRFQCaseId rfqCaseId = conPeek(opportunityData, i); 
            details += rfqCaseId + '\n'; 
        } 
    } 

    return details; 
}
```

<span data-ttu-id="6decd-144">วิธีการนามธรรมที่คงเหลือสองวิธีในการนำไปใช้คือ **provideHealingAction** และ **securityMenuItem**</span><span class="sxs-lookup"><span data-stu-id="6decd-144">The two remaining abstract methods to implement are **provideHealingAction** and **securityMenuItem**.</span></span> 

<span data-ttu-id="6decd-145">**provideHealingAction** ส่งคืนค่าจริง ถ้ามีระบุการดำเนินการรักษามิฉะนั้น จะส่งกลับค่าเท็จ</span><span class="sxs-lookup"><span data-stu-id="6decd-145">**provideHealingAction** returns true if a healing action is provided, otherwise, it returns false.</span></span> <span data-ttu-id="6decd-146">ถ้ามีการส่งคืนค่าจริง วิธีการ **performAction** ต้องถูกนำมาใช้ได้ หรือจะมีข้อผิดพลาดแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="6decd-146">If true is returned, the method **performAction** must be implemented, or an error will be thrown.</span></span> <span data-ttu-id="6decd-147">วิธีการ **performAction** ใช้อาร์กิวเมนต์ **SelfHealingOpportunity** ที่ซึ่งสามารถใช้ข้อมูลสำหรับการดำเนินการได้</span><span class="sxs-lookup"><span data-stu-id="6decd-147">The **performAction** method takes a **SelfHealingOpportunity** argument, in which the data can be used for the action.</span></span> <span data-ttu-id="6decd-148">ในตัวอย่าง การดำเนินการเปิด **PurchRFQCaseTableListPage** สำหรับการแก้ไขด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="6decd-148">In the example, the action opens the **PurchRFQCaseTableListPage**, for manual correction.</span></span> 

```
public boolean providesHealingAction() 
{ 
    return true; 
} 

protected void performAction(SelfHealingOpportunity _opportunity) 
{ 
    new MenuFunction(menuItemDisplayStr(PurchRFQCaseTableListPage), MenuItemType::Display).run(); 
} 
```

<span data-ttu-id="6decd-149">โดยขึ้นอยู่กับข้อกำหนดของกฎ อาจสามารถที่จะดำเนินการโดยอัตโนมัติโดยใช้ข้อมูลโอกาสได้</span><span class="sxs-lookup"><span data-stu-id="6decd-149">Depending on the specifics of the rule, it might be possible to take an automatic action using the opportunity data.</span></span> <span data-ttu-id="6decd-150">ในตัวอย่างนี้ ระบบสามารถสร้างชื่อเรื่องสำหรับกรณี RFQ ได้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="6decd-150">In this example, the system could generate titles for RFQ cases automatically.</span></span> 

<span data-ttu-id="6decd-151">**securityMenuItem** ส่งกลับชื่อของรายการเมนูการดำเนินการ เพื่อให้กฎสามารถมองเห็นได้เฉพาะกับผู้ใช้ที่สามารถเข้าถึงรายการเมนูการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="6decd-151">**securityMenuItem** returns the name of an action menu item such that the rule is only visible to users who can access the action menu item.</span></span> <span data-ttu-id="6decd-152">ความปลอดภัยอาจต้องการให้กฎเฉพาะและโอกาสจะสามารถเข้าถึงผู้ใช้ที่ได้รับอนุญาตเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="6decd-152">Security might require that specific rules and opportunities are accessible only to authorized users.</span></span> <span data-ttu-id="6decd-153">ในตัวอย่าง เฉพาะผู้ใช้ที่มีการเข้าถึง **PurchRFQCaseTitleAction** สามารถดูโอกาสได้</span><span class="sxs-lookup"><span data-stu-id="6decd-153">In the example, only users with access to **PurchRFQCaseTitleAction** can view the opportunity.</span></span> <span data-ttu-id="6decd-154">สังเกตว่า รายการเมนูการดำเนินการนี้ถูกสร้างขึ้นสำหรับตัวอย่างนี้ และถูกเพิ่มเป็นจุดเข้าใช้งานสำหรับสิทธิ์ความปลอดภัย **PurchRFQCaseTableMaintain**</span><span class="sxs-lookup"><span data-stu-id="6decd-154">Notice that this action menu item was created for this example, and was added as an entry point for the **PurchRFQCaseTableMaintain** security privilege.</span></span> 

> [!NOTE]
> <span data-ttu-id="6decd-155">รายการเมนูต้องเป็นรายการเมนูการดำเนินการเพื่อให้ความปลอดภัยทำงานอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="6decd-155">The menu item must be an action menu item for security to work correctly.</span></span> <span data-ttu-id="6decd-156">ชนิดรายการเมนูอื่นๆ เช่น **แสดงรายการเมนู** จะไม่ทำงานอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="6decd-156">Other menu item types, such as **Display menu items** will not work correctly.</span></span>

```
public MenuName securityMenuItem() 
{ 
    return menuItemActionStr(PurchRFQCaseTitleAction); 
}
```

<span data-ttu-id="6decd-157">หลังจากที่มีการคอมไพล์กฎ ดำเนินการงานต่อไปนี้เพื่อให้แสดงในอินเทอร์เฟสผู้ใช้ (UI)</span><span class="sxs-lookup"><span data-stu-id="6decd-157">After the rule has compiled, execute the following job to have it display in the user interface (UI).</span></span>

```
class ScanNewRulesJob 
{         
    public static void main(Args _args) 
    {         
        SysExtensionCache::clearAllScopes(); 
        var controller = new DiagnosticsRuleController(); 
        controller.runOperation(); 
    } 
} 
```

<span data-ttu-id="6decd-158">กฎจะแสดงในแบบฟอร์ม **กฎการตรวจสอบความถูกต้องของการวิเคราะห์** ที่พร้อมใช้งานจาก **การดูแลระบบ** > **งานประจำงวด** > **รักษากฎการตรวจสอบความถูกต้องของการวิเคราะห์**</span><span class="sxs-lookup"><span data-stu-id="6decd-158">The rule will display in the **Diagnostics validation rule** form, available from **System administration** > **Periodic tasks** > **Maintain diagnostics validation rule**.</span></span> <span data-ttu-id="6decd-159">เพื่อการให้มีการประเมิน ไปที่ **การดูแลระบบ** > **งานประจำงวด** > **กฎการตรวจสอบความถูกต้องของการวิเคราะห์ของกำหนดการ** เลือกความถี่ของกฎ เช่น **รายวัน**</span><span class="sxs-lookup"><span data-stu-id="6decd-159">To have it evaluated, go to **System administration** > **Periodic tasks** > **Schedule diagnostics validation rule**, select the frequency of the rule, such as **Daily**.</span></span> <span data-ttu-id="6decd-160">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="6decd-160">Click **OK**.</span></span> <span data-ttu-id="6decd-161">ไปยัง **การดูแลระบบ** > **โปรแกรมช่วยแนะนำการปรับให้เหมาะสม** เพื่อดูโอกาสใหม่</span><span class="sxs-lookup"><span data-stu-id="6decd-161">Go to **System administration** > **Optimization advisor** to view the new opportunity.</span></span> 

<span data-ttu-id="6decd-162">ตัวอย่างต่อไปนี้คือ ส่วนเล็กๆ ของโค้ดที่มีโครงสร้างของกฎซึ่งรวมถึงวิธีและแอททริบิวต์ที่จำเป็นทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="6decd-162">The following example is a code snippet with the skeleton of a rule including all the required methods and attributes.</span></span> <span data-ttu-id="6decd-163">จะช่วยคุณในการเริ่มต้นใช้งานด้วยการเขียนกฎใหม่</span><span class="sxs-lookup"><span data-stu-id="6decd-163">It helps you get started with writing new rules.</span></span><span data-ttu-id="6decd-164"> ฉลากและรายการเมนูการดำเนินการที่ถูกใช้ในตัวอย่าง ถูกใช้เพื่อวัตถุประสงค์การสาธิตเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="6decd-164"> The labels and action menu items that are used in the example are only used for demonstration purpose.</span></span>

```
[DiagnosticsRuleAttribute]
public final class SkeletonSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule
{
    [DiagnosticsRuleSubscription(DiagnosticsArea::SCM,
                                 "@SkeletonRuleLabels:SkeletonRuleTitle", // Label with the title of the rule
                                 DiagnosticsRunFrequency::Monthly,
                                 "@SkeletonRuleLabels:SkeletonRuleDescription")] // Label with a description of the rule
    public str opportunityTitle()
    {
        // Return a label with the title of the opportunity
        return "@SkeletonRuleLabels:SkeletonOpportunityTitle";
    }

    public str opportunityDetails(SelfHealingOpportunity _opportunity)
    {
        str details = "";

        // Use _opportunity.data to provide details on the opportunity

        return details;
    }

    protected List evaluate()
    {
        List results = new List(Types::Record);

        // Write here the core logic of the rule

        // When creating an opportunity, use:
        //     * this.getOpportunityForCompany() for company specific opportunities
        //     * this.getOpportunityAcrossCompanies() for cross-company opportunities

        return results;
    }

    public boolean providesHealingAction()
    {
        return true;
    }

    protected void performAction(SelfHealingOpportunity _opportunity)
    {
        // Place here the code that performs the healing action

        // To open a form, use the following:
        // new MenuFunction(menuItemDisplayStr(SkeletonRuleDisplayMenuItem), MenuItemType::Display).run();
    }

    public MenuName securityMenuItem()
    {
        return menuItemActionStr(SkeletonRuleActionMenuItem);
    }

}
```

<span data-ttu-id="6decd-165">สำหรับข้อมูลเพิ่มเติม ดูวิดีโอ YouTube แบบสั้น: [ผู้แนะนำการเพิ่มประสิทธิภาพใน Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=MRsAzgFCUSQ)</span><span class="sxs-lookup"><span data-stu-id="6decd-165">For more information, watch the short YouTube video: [Optimization advisor in Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=MRsAzgFCUSQ)</span></span>
