pm.test("Status code is 200", function () {


pm.test("Check pet  ID", function () {
    var jsonData = pm.response.json();
    pm.expect(jsonData.id).to.eql(9223372036854775807);
});
    pm.response.to.have.status(200);
});
pm.test("check pet name", function () {
    var jsonData = pm.response.json();
    pm.expect(jsonData.name).to.eql("doggie");
});

pm.test("check pet status", function () {
    var jsonData = pm.response.json();
    pm.expect(jsonData.status).to.eql("available");
});


