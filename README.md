//Identification and Reconciliation Engine (IRE) do ServiceNow para criar ou atualizar um CI.


var payload = {
    "items": [
        {
            "className": "cmdb_ci_win_server",
            "values": {
                "short_description": "Updated by Manual Entry",
                "name": "snow911",
                "ram": 1092,
                "serial_number": "0000-0011-6608-7808-9234-0119-27"
            }
        }
    ]
};

var input = new JSON().encode(payload);

var output = SNC.IdentificationEngineScriptableApi.createOrUpdateCI(
    'Manual Entry',
    input
);

gs.print(JSON.stringify(output));
