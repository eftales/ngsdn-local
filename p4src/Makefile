BMV2_SWITCH_EXE = simple_switch_grpc
TOPO = topology.json
onos_curl := curl --fail -sSL --user onos:rocks --noproxy localhost
onos_url := http://localhost:8181/onos

include utils/Makefile

cp:
	rm -rf ../app/src/main/resources
	mkdir -p ../app/src/main/resources
	cp build/* ../app/src/main/resources/

netcfg:
	${onos_curl} -X POST -H 'Content-Type:application/json' \
		${onos_url}/v1/network/configuration -d@netcfg.json
