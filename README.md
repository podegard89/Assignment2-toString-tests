# Assignment2-toString-tests
    @Test
    public void testToStringIsFormattedProperly() {
        Job testJob = new Job("Product tester", new Employer("ACME"), new Location("Desert"), new PositionType("Quality control"), new CoreCompetency("Persistence"));
        String expectedToStringOutput =
                "ID: 1\n" +
                "Name: Product tester\n" +
                "Employer: ACME\n" +
                "Location: Desert\n" +
                "Position Type: Quality Control\n" +
                "Core Competency: Persistence\n";
        Assertions.assertEquals(expectedToStringOutput, testJob.toString());

    }

    @Test
    public void testToStringDataNotAvailable() {
        Job testJob = new Job("Software Eng. 1", new Employer(""), new Location(""), new PositionType(""), new CoreCompetency(""));
        String expectedToStringOutput =
                "ID: 1\n" +
                "Name: Software Eng. 1\n" +
                "Employer: Data not available\n" +
                "Location: Data not available\n" +
                "Position Type: Data not available\n" +
                "Core Competency: Data not available\n";
        Assertions.assertEquals(expectedToStringOutput, testJob.toString());
    }
