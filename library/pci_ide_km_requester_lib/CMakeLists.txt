cmake_minimum_required(VERSION 2.6)

INCLUDE_DIRECTORIES(${LIBSPDM_DIR}/include
                    ${LIBSPDM_DIR}/include/hal/${ARCH}
                    ${PROJECT_SOURCE_DIR}/include
)

SET(src_pci_ide_km_requester_lib
    pci_ide_km_send_receive.c
    pci_ide_km_req_query.c
    pci_ide_km_req_key_prog.c
    pci_ide_km_req_key_set_go.c
    pci_ide_km_req_key_set_stop.c
)

ADD_LIBRARY(pci_ide_km_requester_lib STATIC ${src_pci_ide_km_requester_lib})
