import org.junit.jupiter.api.Test;
import static org.junit.jupiter.api.Assertions.*;

public class DomainObjectsTest {

    @Test
    public void testImmigrantSubmission() {
        Immigrant immigrant = new Immigrant("ID001", "John Doe", "1990-01-01", "USA");
        immigrant.submitMedicalCondition();
        assertNotNull(immigrant, "Immigrant should not be null after submission.");
    }

    @Test
    public void testMedicalConditionValidation() {
        MedicalCondition condition = new MedicalCondition("C001", "Flu", false);
        condition.validateCondition();
        assertEquals("Flu", condition.conditionName, "Condition name should match.");
    }

    @Test
    public void testInfectiousDiseaseNotification() {
        InfectiousDisease disease = new InfectiousDisease("C002", "COVID-19", true, true);
        disease.notifyHealthAuthority();
        assertTrue(disease.isInfectious, "Disease should be infectious.");
    }

    @Test
    public void testWorkflowTableAssignment() {
        WorkflowTable workflow = new WorkflowTable("W001", "In Progress", "John");
        workflow.assignToNextStage();
        assertEquals("In Progress", workflow.currentStatus, "Workflow status should be updated.");
    }

    @Test
    public void testValidatorSubmission() {
        String[] rules = {"Rule1", "Rule2"};
        Validator validator = new Validator("V001", rules);
        validator.validateSubmission();
        assertEquals(2, validator.validationRules.length, "Validator should have two rules.");
    }
}
