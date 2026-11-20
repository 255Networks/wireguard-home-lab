# Validation plan

Use a personally controlled client, an independent internet connection and a private test service with a known response. The original troubleshooting notes provide the starting observations. The checks below are proposed follow-up work. Each result remains open until its evidence is available.

| Check | Control and comparison | Evidence needed to record a pass | Current status |
| --- | --- | --- | --- |
| Local service health | From inside the home network, request one known resource from the test service. | Timestamp and expected response from the intended service. | Pending |
| Off-site tunnel handshake | From the independent connection, record peer status before the test, initiate a new connection and check status on both sides. | Fresh, corresponding handshake times and traffic counters advancing during the test. | Pending |
| Private-service reachability | From the same off-site client, request the known resource once with the tunnel off and again with it on. | Success only with the tunnel active. If the service is reachable in both runs, investigate the control before drawing a conclusion. | Pending |
| DNS path | Use distinct, uncached test names under a controlled domain in a tunnel-off and tunnel-on run. Compare client observations with the intended resolver's query record. | A timestamped match between the tunnel-on query and the intended resolver's record. Record both results even when they agree. | Pending |
| Separate exit-node comparison | On the same Mac and access network, use the same address-check service and address family with the comparison exit node deselected, then selected. | Record whether the selected run matches the independently observed exit-node egress address. Document the result separately from WireGuard reachability. | Pending |

## Interpreting a partial result

- If local service health fails, restore a known-good service baseline before interpreting a remote request.
- If a fresh tunnel handshake succeeds and the private service stays unreachable, investigate routing and service access as separate questions.
- If a client-side DNS display differs from expectations, record which query reached the intended resolver before attributing a cause.
- Keep the original timestamp and detailed records privately. A public update can identify the check, month, pass or fail, and the evidence type using role labels.

## Evidence entry for a future run

| Date and time (UTC) | Check | Baseline result | Test result | Evidence reference | Conclusion |
| --- | --- | --- | --- | --- | --- |
| To be recorded | | | | | |
