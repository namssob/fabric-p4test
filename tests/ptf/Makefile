PTF_BMV2_CMD = sudo ./ptf_runner.py --device bmv2 --port-map port_map.veth.json --ptf-dir fabric.ptf
BASE_P4C_OUT_PATH = ${ONOS_ROOT}/pipelines/fabric/src/main/resources/p4c-out
FABRIC_OUT = ${BASE_P4C_OUT_PATH}/fabric/bmv2/default
FABRIC_SPGW_OUT = ${BASE_P4C_OUT_PATH}/fabric-spgw/bmv2/default

all: fabric fabric-spgw

fabric:
	${PTF_BMV2_CMD} \
		--p4info ${FABRIC_OUT}/p4info.txt \
		--bmv2-json ${FABRIC_OUT}/bmv2.json \
		all ^spgw

fabric-spgw:
	${PTF_BMV2_CMD} \
		--p4info ${FABRIC_SPGW_OUT}/p4info.txt \
		--bmv2-json ${FABRIC_SPGW_OUT}/bmv2.json \
		all
