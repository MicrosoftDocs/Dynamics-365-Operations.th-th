---
title: สร้างกฎสำหรับโปรแกรมช่วยแนะนำการปรับให้เหมาะสม
description: หัวข้อนี้อธิบายวิธีการเพิ่มกฎใหม่ในโปรแกรมช่วยแนะนำการปรับให้เหมาะสม
author: roxanadiaconu
manager: AnnBe
ms.date: 02/04/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SelfHealingWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: sericks
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 67e740a1e00c425f0e09b5f0fc960cf2778efd89
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568297"
---
# <a name="create-rules-for-optimization-advisor"></a>สร้างกฎสำหรับโปรแกรมช่วยแนะนำการปรับให้เหมาะสม

[!include [banner](../includes/banner.md)]

หัวข้อนี้อธิบายวิธีการสร้างกฎใหม่สำหรับ **โปรแกรมช่วยแนะนำการปรับให้เหมาะสม** ตัวอย่างเช่น คุณสามารถสร้างกฎใหม่ที่ระบุกรณีของคำขอใบเสนอราคา (RFQ) ที่มีชื่อเรื่องแบบว่างเปล่า การใช้ชื่อในกรณีทำให้สามารถระบุและสามารถค้นหาได้ง่าย ขณะที่ค่อนข้างอย่างง่าย ตัวอย่างนี้แสดงสิ่งที่สามารถทำได้ด้วยกฎการปรับให้เหมาะสม 

*กฎ* เป็นการตรวจสอบข้อมูลแอพลิเคชัน ถ้าเป็นไปตามเงื่อนไขที่กฎประเมิน จะมีการสร้างโอกาสในการเพิ่มประสิทธิภาพกระบวนการ หรือปรับปรุงข้อมูล โอกาสที่สามารถดำเนินการ และอีกทางหนึ่งคือ สามารถวัดผลกระทบของการดำเนินการได้ 

ในการสร้างกฎใหม่สำหรับ **โปรแกรมช่วยแนะนำการปรับให้เหมาะสม** เพิ่มคลาสใหม่ที่ขยายคลาสนามธรรม **SelfHealingRule** ใช้อินเทอร์เฟส **IDiagnosticsRule** และถูกตกแต่งโดยแอตทริบิวต์ **DiagnosticRule** คลาสต้องมีวิธีที่ถูกตกแต่งด้วยแอตทริบิวต์ **DiagnosticsRuleSubscription** ตามแบบแผน ซึ่งเสร็จสิ้นในวิธี **opportunityTitle** ซึ่งจะกล่าวถึงในภายหลัง คลาสใหม่นี้สามารถถูกเพิ่มไปยังแบบจำลองที่กำหนดเองที่มีการขึ้นต่อกันในแบบจำลอง **SelfHealingRules** ได้ ในตัวอย่างต่อไปนี้ กฎที่กำลังถูกใช้ เรียกว่า **RFQTitleSelfHealingRule**

```xpp
[DiagnosticsRule] 
public final class RFQTitleSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule 
{ 
… 
} 
```

คลาสนามธรรม **SelfHealingRule** มีวิธีการนามธรรมที่ต้องดำเนินการในคลาสที่สืบทอด หลักคือ วิธี **ประเมิน** ซึ่งส่งกลับรายการของโอกาสที่ระบุโดยกฎ โอกาสสามารถเป็นต่อนิติบุคคล หรือสามารถนำไปใช้กับทั้งระบบได้

```xpp
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

วิธีการที่แสดงไว้ข้างบนวนผ่านบริษัทและเลือกกรณี RFQ ที่มีชื่อเรื่องแบบว่างเปล่าในวิธี **findRFQCasesWithEmptyTitle** ถ้ามีการพบกรณีดังกล่าวอย่างน้อยหนึ่งกรณี โอกาสทางการขายเฉพาะบริษัทจะถูกสร้างขึ้นด้วยวิธี **getOpportunityForCompany** สังเกตว่า ฟิลด์ **ข้อมูล** ในตาราง **SelfHealingOpportunity** เป็นชนิด **คอนเทนเนอร์** และดังนั้นจึงสามารถประกอบด้วยข้อมูลที่เกี่ยวข้องกับตรรกะเฉพาะสำหรับกฎนี้ การตั้งค่า **OpportunityDate** ด้วยการประทับเวลาปัจจุบันจะลงทะเบียนเวลาของการประเมินล่าสุดของโอกาส  

โอกาสทางการขายอาจเป็นระหว่างบริษัทได้ด้วย ในกรณีนี้ ลูปที่ผ่านบริษัทไม่จำเป็น และต้องมีการสร้างโอกาสด้วยวิธี **getOpportunityAcrossCompanies** 

โค้ดต่อไปนี้แสดงวิธี **findRFQCasesWithEmptyTitle** ซึ่งส่งกลับรหัสของกรณี RFQ ที่มีชื่อที่ว่างเปล่า

```xpp
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

วิธีเพิ่มเติมที่ต้องถูกนำมาใช้คือ **opportunityTitle** และ **opportunityDetails** ค่าเดิมคืนค่าชื่อเรื่องแบบสั้นสำหรับโอกาส ค่าหลังส่งคืนคำอธิบายโดยละเอียดของโอกาสทางการขาย ซึ่งยังสามารถมีข้อมูลอยู่ได้ด้วย

ชื่อเรื่องที่ส่งคืนโดย **opportunityTitle** ปรากฏอยู่ภายใต้คอลัมน์ **โอกาสในการปรับให้เหมาะสม** ในพื้นที่ทำงาน **โปรแกรมช่วยแนะนำการปรับให้เหมาะสม** นอกจากนี้ยังปรากฏเป็นส่วนหัวของบานหน้าต่างด้านข้างที่แสดงข้อมูลเพิ่มเติมเกี่ยวกับโอกาสด้วย ตามแบบแผน วิธีการนี้ถูกปรับปรุงด้วยแอตทริบิวต์ **DiagnosticRuleSubscription** ซึ่งใช้อาร์กิวเมนต์ดังต่อไปนี้: 

* **พื้นที่วินิจฉัย** – enum ของชนิด **DiagnosticArea** ที่อธิบายว่าพื้นที่ใดของแอพลิเคชันที่มีกฎอยู่ เช่น **DiagnosticArea::SCM** 

* **ชื่อกฎ** – สตริงที่มีชื่อกฎ นี่จะปรากฏขึ้นภายใต้คอลัมน์ **ชื่อกฎ** ในแบบฟอร์ม **กฎการตรวจสอบความถูกต้องของการวิเคราะห์** (**DiagnosticsValidationRuleMaintain**) 

* **ความถี่ในการรัน** – enum ของชนิด **DiagnosticRunFrequency** ที่อธิบายความถี่ที่กฎควรถูกรัน เช่น **DiagnosticRunFrequency::รายวัน** 

* **คำอธิบายกฎ** – สตริงที่มีคำอธิบายโดยละเอียดมากขึ้นของกฎ นี่จะปรากฏขึ้นภายใต้คอลัมน์ **คำอธิบายกฎ** ในแบบฟอร์ม **กฎการตรวจสอบความถูกต้องของการวิเคราะห์** (**DiagnosticsValidationRuleMaintain**) 

> [!NOTE]
> แอททริบิวต์ **DiagnosticRuleSubscription** จำเป็นสำหรับกฎในการทำงาน โดยทั่วไป จะมีการใช้ใน **opportunityTitle** แต่จะสามารถตกแต่งวิธีใดๆ ของคลาสได้

รายการต่อไปนี้เป็นการนำไปใช้แบบตัวอย่าง มีการใช้สตริงการดิบสำหรับความเรียบง่าย แต่การใช้งานที่ถูกต้องต้องมีป้ายชื่อ 

```xpp
[DiagnosticsRuleSubscription(DiagnosticsArea::SCM, 
                             'Assign titles to Request for Quotation cases', 
                             DiagnosticsRunFrequency::Daily,  
                             'This rule detects Requests for Quotation with empty titles.')] 
public str opportunityTitle() 
{ 
    return 'Assign titles to Request for Quotation cases'; 
} 
```

คำอธิบายที่ส่งคืนโดย **opportunityDetails** ปรากฏในบานหน้าต่างด้านข้างที่แสดงข้อมูลเพิ่มเติมเกี่ยวกับโอกาส นี่จะใช้อาร์กิวเมนต์ **SelfHealingOpportunity** ซึ่งก็คือฟิลด์ **ข้อมูล** ที่สามารถใช้เพื่อระบุรายละเอียดเพิ่มเติมเกี่ยวกับโอกาสได้ ในตัวอย่าง วิธีส่งคืนรหัสของกรณี RFQ ที่มีชื่อเรื่องแบบว่างเปล่า 

```xpp
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

วิธีการนามธรรมที่คงเหลือสองวิธีในการนำไปใช้คือ **provideHealingAction** และ **securityMenuItem** 

**provideHealingAction** ส่งคืนค่าจริง ถ้ามีระบุการดำเนินการรักษามิฉะนั้น จะส่งกลับค่าเท็จ ถ้ามีการส่งคืนค่าจริง วิธีการ **performAction** ต้องถูกนำมาใช้ได้ หรือจะมีข้อผิดพลาดแสดงขึ้น วิธีการ **performAction** ใช้อาร์กิวเมนต์ **SelfHealingOpportunity** ที่ซึ่งสามารถใช้ข้อมูลสำหรับการดำเนินการได้ ในตัวอย่าง การดำเนินการเปิด **PurchRFQCaseTableListPage** สำหรับการแก้ไขด้วยตนเอง 

```xpp
public boolean providesHealingAction() 
{ 
    return true; 
} 

protected void performAction(SelfHealingOpportunity _opportunity) 
{ 
    new MenuFunction(menuItemDisplayStr(PurchRFQCaseTableListPage), MenuItemType::Display).run(); 
} 
```

โดยขึ้นอยู่กับข้อกำหนดของกฎ อาจสามารถที่จะดำเนินการโดยอัตโนมัติโดยใช้ข้อมูลโอกาสได้ ในตัวอย่างนี้ ระบบสามารถสร้างชื่อเรื่องสำหรับกรณี RFQ ได้โดยอัตโนมัติ 

**securityMenuItem** ส่งกลับชื่อของรายการเมนูการดำเนินการ เพื่อให้กฎสามารถมองเห็นได้เฉพาะกับผู้ใช้ที่สามารถเข้าถึงรายการเมนูการดำเนินการ ความปลอดภัยอาจต้องการให้กฎเฉพาะและโอกาสจะสามารถเข้าถึงผู้ใช้ที่ได้รับอนุญาตเท่านั้น ในตัวอย่าง เฉพาะผู้ใช้ที่มีการเข้าถึง **PurchRFQCaseTitleAction** สามารถดูโอกาสได้ สังเกตว่า รายการเมนูการดำเนินการนี้ถูกสร้างขึ้นสำหรับตัวอย่างนี้ และถูกเพิ่มเป็นจุดเข้าใช้งานสำหรับสิทธิ์ความปลอดภัย **PurchRFQCaseTableMaintain** 

> [!NOTE]
> รายการเมนูต้องเป็นรายการเมนูการดำเนินการเพื่อให้ความปลอดภัยทำงานอย่างถูกต้อง ชนิดรายการเมนูอื่นๆ เช่น **แสดงรายการเมนู** จะไม่ทำงานอย่างถูกต้อง

```xpp
public MenuName securityMenuItem() 
{ 
    return menuItemActionStr(PurchRFQCaseTitleAction); 
}
```

หลังจากที่มีการคอมไพล์กฎ ดำเนินการงานต่อไปนี้เพื่อให้แสดงในอินเทอร์เฟสผู้ใช้ (UI)

```xpp
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

กฎจะแสดงในแบบฟอร์ม **กฎการตรวจสอบความถูกต้องของการวิเคราะห์** ที่พร้อมใช้งานจาก **การดูแลระบบ** > **งานประจำงวด** > **รักษากฎการตรวจสอบความถูกต้องของการวิเคราะห์** เพื่อการให้มีการประเมิน ไปที่ **การดูแลระบบ** > **งานประจำงวด** > **กฎการตรวจสอบความถูกต้องของการวิเคราะห์ของกำหนดการ** เลือกความถี่ของกฎ เช่น **รายวัน** คลิก **ตกลง**  ไปยัง **การดูแลระบบ** > **โปรแกรมช่วยแนะนำการปรับให้เหมาะสม** เพื่อดูโอกาสใหม่ 

ตัวอย่างต่อไปนี้คือ ส่วนเล็กๆ ของโค้ดที่มีโครงสร้างของกฎซึ่งรวมถึงวิธีและแอททริบิวต์ที่จำเป็นทั้งหมด จะช่วยคุณในการเริ่มต้นใช้งานด้วยการเขียนกฎใหม่ ฉลากและรายการเมนูการดำเนินการที่ถูกใช้ในตัวอย่าง ถูกใช้เพื่อวัตถุประสงค์การสาธิตเท่านั้น

```xpp
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

สำหรับข้อมูลเพิ่มเติม ดูวิดีโอ YouTube แบบสั้น: [ผู้แนะนำการเพิ่มประสิทธิภาพใน Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=MRsAzgFCUSQ)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]