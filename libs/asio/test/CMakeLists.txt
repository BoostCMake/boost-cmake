include(CMTest)

cm_test_link_libraries(${CMAKE_WORKSPACE_NAME}_asio
                        )

#
# Copyright (c) 2003-2017 Christopher M. Kohlhoff (chris at kohlhoff dot com)
#
# Distributed under the Boost Software License, Version 1.0. (See accompanying
# file LICENSE_1_0.txt or copy at http://www.boost.org/LICENSE_1_0.txt)
#

set(USE_SELECT "-DBOOST_ASIO_DISABLE_DEV_POLL -DBOOST_ASIO_DISABLE_EPOLL -DBOOST_ASIO_DISABLE_KQUEUE -DBOOST_ASIO_DISABLE_IOCP")

#test-suite "asio"
cm_test(NAME asio_test_basic_datagram_socket SOURCES ${CURRENT_TEST_SOURCES_DIR}/basic_datagram_socket.cpp COMPILE_ONLY)
cm_test(NAME asio_test_basic_datagram_socket_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/basic_datagram_socket.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_basic_datagram_socket_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_basic_deadline_timer SOURCES ${CURRENT_TEST_SOURCES_DIR}/basic_deadline_timer.cpp COMPILE_ONLY)
cm_test(NAME asio_test_basic_deadline_timer_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/basic_deadline_timer.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_basic_deadline_timer_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_basic_raw_socket SOURCES ${CURRENT_TEST_SOURCES_DIR}/basic_raw_socket.cpp COMPILE_ONLY)
cm_test(NAME asio_test_basic_raw_socket_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/basic_raw_socket.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_basic_raw_socket_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_basic_seq_packet_socket SOURCES ${CURRENT_TEST_SOURCES_DIR}/basic_seq_packet_socket.cpp COMPILE_ONLY)
cm_test(NAME asio_test_basic_seq_packet_socket_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/basic_seq_packet_socket.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_basic_seq_packet_socket_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_basic_signal_set SOURCES ${CURRENT_TEST_SOURCES_DIR}/basic_signal_set.cpp COMPILE_ONLY)
cm_test(NAME asio_test_basic_signal_set_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/basic_signal_set.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_basic_signal_set_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_basic_socket_acceptor SOURCES ${CURRENT_TEST_SOURCES_DIR}/basic_socket_acceptor.cpp COMPILE_ONLY)
cm_test(NAME asio_test_basic_socket_acceptor_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/basic_socket_acceptor.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_basic_socket_acceptor_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_basic_stream_socket SOURCES ${CURRENT_TEST_SOURCES_DIR}/basic_stream_socket.cpp COMPILE_ONLY)
cm_test(NAME asio_test_basic_stream_socket_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/basic_stream_socket.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_basic_stream_socket_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_basic_streambuf SOURCES ${CURRENT_TEST_SOURCES_DIR}/basic_streambuf.cpp COMPILE_ONLY)
cm_test(NAME asio_test_basic_streambuf_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/basic_streambuf.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_basic_streambuf_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_basic_waitable_timer SOURCES ${CURRENT_TEST_SOURCES_DIR}/basic_waitable_timer.cpp COMPILE_ONLY)
cm_test(NAME asio_test_basic_waitable_timer_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/basic_waitable_timer.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_basic_waitable_timer_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_buffer SOURCES ${CURRENT_TEST_SOURCES_DIR}/buffer.cpp)
cm_test(NAME asio_test_buffer_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/buffer.cpp)
target_compile_definitions(asio_test_buffer_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_buffered_read_stream SOURCES ${CURRENT_TEST_SOURCES_DIR}/buffered_read_stream.cpp)
cm_test(NAME asio_test_buffered_read_stream_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/buffered_read_stream.cpp)
target_compile_definitions(asio_test_buffered_read_stream_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_buffered_stream SOURCES ${CURRENT_TEST_SOURCES_DIR}/buffered_stream.cpp)
cm_test(NAME asio_test_buffered_stream_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/buffered_stream.cpp)
target_compile_definitions(asio_test_buffered_stream_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_buffered_write_stream SOURCES ${CURRENT_TEST_SOURCES_DIR}/buffered_write_stream.cpp)
cm_test(NAME asio_test_buffered_write_stream_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/buffered_write_stream.cpp)
target_compile_definitions(asio_test_buffered_write_stream_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_buffers_iterator SOURCES ${CURRENT_TEST_SOURCES_DIR}/buffers_iterator.cpp)
cm_test(NAME asio_test_buffers_iterator_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/buffers_iterator.cpp)
target_compile_definitions(asio_test_buffers_iterator_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_completion_condition SOURCES ${CURRENT_TEST_SOURCES_DIR}/completion_condition.cpp COMPILE_ONLY)
cm_test(NAME asio_test_completion_condition_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/completion_condition.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_completion_condition_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_connect SOURCES ${CURRENT_TEST_SOURCES_DIR}/connect.cpp COMPILE_ONLY)
cm_test(NAME asio_test_connect_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/connect.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_connect_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_coroutine SOURCES ${CURRENT_TEST_SOURCES_DIR}/coroutine.cpp COMPILE_ONLY)
cm_test(NAME asio_test_coroutine_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/coroutine.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_coroutine_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_datagram_socket_service SOURCES ${CURRENT_TEST_SOURCES_DIR}/datagram_socket_service.cpp COMPILE_ONLY)
cm_test(NAME asio_test_datagram_socket_service_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/datagram_socket_service.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_datagram_socket_service_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_deadline_timer_service SOURCES ${CURRENT_TEST_SOURCES_DIR}/deadline_timer_service.cpp COMPILE_ONLY)
cm_test(NAME asio_test_deadline_timer_service_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/deadline_timer_service.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_connect_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_deadline_timer SOURCES ${CURRENT_TEST_SOURCES_DIR}/deadline_timer.cpp)
cm_test(NAME asio_test_deadline_timer_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/deadline_timer.cpp)
target_compile_definitions(asio_test_deadline_timer_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_asio_error SOURCES ${CURRENT_TEST_SOURCES_DIR}/error.cpp)
cm_test(NAME asio_test_asio_error_seletc SOURCES ${CURRENT_TEST_SOURCES_DIR}/error.cpp)
target_compile_definitions(asio_test_asio_error_seletc PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_generic_basic_endpoint SOURCES ${CURRENT_TEST_SOURCES_DIR}/generic/basic_endpoint.cpp COMPILE_ONLY)
cm_test(NAME asio_test_generic_basic_endpoint_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/generic/basic_endpoint.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_generic_basic_endpoint_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_generic_datagram_protocol SOURCES ${CURRENT_TEST_SOURCES_DIR}/generic/datagram_protocol.cpp COMPILE_ONLY)
cm_test(NAME asio_test_generic_datagram_protocol_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/generic/datagram_protocol.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_generic_datagram_protocol_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_generic_raw_protocol SOURCES ${CURRENT_TEST_SOURCES_DIR}/generic/raw_protocol.cpp COMPILE_ONLY)
cm_test(NAME asio_test_generic_raw_protocol_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/generic/raw_protocol.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_generic_raw_protocol_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_generic_seq_packet_protocol SOURCES ${CURRENT_TEST_SOURCES_DIR}/generic/seq_packet_protocol.cpp COMPILE_ONLY)
cm_test(NAME asio_test_generic_seq_packet_protocol_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/generic/seq_packet_protocol.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_generic_seq_packet_protocol_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_generic_stream_protocol SOURCES ${CURRENT_TEST_SOURCES_DIR}/generic/stream_protocol.cpp COMPILE_ONLY)
cm_test(NAME asio_test_generic_stream_protocol_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/generic/stream_protocol.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_generic_stream_protocol_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_high_resolution_timer SOURCES ${CURRENT_TEST_SOURCES_DIR}/high_resolution_timer.cpp COMPILE_ONLY)
cm_test(NAME asio_test_high_resolution_timer_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/high_resolution_timer.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_high_resolution_timer_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_io_service SOURCES ${CURRENT_TEST_SOURCES_DIR}/io_service.cpp)
cm_test(NAME asio_test_io_service_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/io_service.cpp)
target_compile_definitions(asio_test_io_service_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_ip_address SOURCES ${CURRENT_TEST_SOURCES_DIR}/ip/address.cpp COMPILE_ONLY)
cm_test(NAME asio_test_ip_address_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/ip/address.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_ip_address_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_ip_address_v4 SOURCES ${CURRENT_TEST_SOURCES_DIR}/ip/address_v4.cpp COMPILE_ONLY)
cm_test(NAME asio_test_ip_address_v4_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/ip/address_v4.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_ip_address_v4_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_ip_address_v6 SOURCES ${CURRENT_TEST_SOURCES_DIR}/ip/address_v6.cpp COMPILE_ONLY)
cm_test(NAME asio_test_ip_address_v6_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/ip/address_v6.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_ip_address_v6_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_ip_basic_endpoint SOURCES ${CURRENT_TEST_SOURCES_DIR}/ip/basic_endpoint.cpp COMPILE_ONLY)
cm_test(NAME asio_test_ip_basic_endpoint_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/ip/basic_endpoint.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_ip_basic_endpoint_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_ip_basic_resolver SOURCES ${CURRENT_TEST_SOURCES_DIR}/ip/basic_resolver.cpp COMPILE_ONLY)
cm_test(NAME asio_test_ip_basic_resolver_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/ip/basic_resolver.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_ip_basic_resolver_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_ip_basic_resolver_entry SOURCES ${CURRENT_TEST_SOURCES_DIR}/ip/basic_resolver_entry.cpp COMPILE_ONLY)
cm_test(NAME asio_test_ip_basic_resolver_entry_seletc SOURCES ${CURRENT_TEST_SOURCES_DIR}/ip/basic_resolver_entry.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_ip_basic_resolver_entry_seletc PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_ip_basic_resolver_iterator SOURCES ${CURRENT_TEST_SOURCES_DIR}/ip/basic_resolver_iterator.cpp COMPILE_ONLY)
cm_test(NAME asio_test_ip_basic_resolver_iterator_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/ip/basic_resolver_iterator.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_ip_basic_resolver_iterator_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_ip_basic_resolver_query SOURCES ${CURRENT_TEST_SOURCES_DIR}/ip/basic_resolver_query.cpp COMPILE_ONLY)
cm_test(NAME asio_test_ip_basic_resolver_query_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/ip/basic_resolver_query.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_ip_basic_resolver_query_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_ip_host_name SOURCES ${CURRENT_TEST_SOURCES_DIR}/ip/host_name.cpp)
cm_test(NAME asio_test_ip_host_name_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/ip/host_name.cpp)
target_compile_definitions(asio_test_ip_host_name_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_ip_icmp SOURCES ${CURRENT_TEST_SOURCES_DIR}/ip/icmp.cpp)
cm_test(NAME asio_test_ip_icmp_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/ip/icmp.cpp)
target_compile_definitions(asio_test_ip_icmp_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_ip_multicast SOURCES ${CURRENT_TEST_SOURCES_DIR}/ip/multicast.cpp)
cm_test(NAME asio_test_ip_multicast_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/ip/multicast.cpp)
target_compile_definitions(asio_test_ip_multicast_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_ip_resolver_query_base SOURCES ${CURRENT_TEST_SOURCES_DIR}/ip/resolver_query_base.cpp COMPILE_ONLY)
cm_test(NAME asio_test_ip_resolver_query_base_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/ip/resolver_query_base.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_ip_resolver_query_base_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_ip_resolver_service SOURCES ${CURRENT_TEST_SOURCES_DIR}/ip/resolver_service.cpp COMPILE_ONLY)
cm_test(NAME asio_test_ip_resolver_service_seletc SOURCES ${CURRENT_TEST_SOURCES_DIR}/ip/resolver_service.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_ip_resolver_service_seletc PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_ip_tcp SOURCES ${CURRENT_TEST_SOURCES_DIR}/ip/tcp.cpp)
cm_test(NAME asio_test_ip_tcp_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/ip/tcp.cpp)
target_compile_definitions(asio_test_ip_tcp_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_ip_udp SOURCES ${CURRENT_TEST_SOURCES_DIR}/ip/udp.cpp)
cm_test(NAME asio_test_ip_udp_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/ip/udp.cpp)
target_compile_definitions(asio_test_ip_udp_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_ip_unicast SOURCES ${CURRENT_TEST_SOURCES_DIR}/ip/unicast.cpp)
cm_test(NAME asio_test_ip_unicast_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/ip/unicast.cpp)
target_compile_definitions(asio_test_ip_unicast_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_ip_v6_only SOURCES ${CURRENT_TEST_SOURCES_DIR}/ip/v6_only.cpp)
cm_test(NAME asio_test_ip_v6_only_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/ip/v6_only.cpp)
target_compile_definitions(asio_test_ip_v6_only_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_is_read_buffered SOURCES ${CURRENT_TEST_SOURCES_DIR}/is_read_buffered.cpp)
cm_test(NAME asio_test_is_read_buffered_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/is_read_buffered.cpp)
target_compile_definitions(asio_test_is_read_buffered_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_is_write_buffered SOURCES ${CURRENT_TEST_SOURCES_DIR}/is_write_buffered.cpp)
cm_test(NAME asio_test_is_write_buffered_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/is_write_buffered.cpp)
target_compile_definitions(asio_test_is_write_buffered_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_local_basic_endpoint SOURCES ${CURRENT_TEST_SOURCES_DIR}/local/basic_endpoint.cpp COMPILE_ONLY)
cm_test(NAME asio_test_local_basic_endpoint_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/local/basic_endpoint.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_local_basic_endpoint_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_local_connect_pair SOURCES ${CURRENT_TEST_SOURCES_DIR}/local/connect_pair.cpp COMPILE_ONLY)
cm_test(NAME asio_test_local_connect_pair_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/local/connect_pair.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_local_connect_pair_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_local_datagram_protocol SOURCES ${CURRENT_TEST_SOURCES_DIR}/local/datagram_protocol.cpp COMPILE_ONLY)
cm_test(NAME asio_test_local_datagram_protocol_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/local/datagram_protocol.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_local_datagram_protocol_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_local_stream_protocol SOURCES ${CURRENT_TEST_SOURCES_DIR}/local/stream_protocol.cpp COMPILE_ONLY)
cm_test(NAME asio_test_local_stream_protocol_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/local/stream_protocol.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_local_stream_protocol_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_placeholders SOURCES ${CURRENT_TEST_SOURCES_DIR}/placeholders.cpp COMPILE_ONLY)
cm_test(NAME asio_test_placeholders_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/placeholders.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_placeholders_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_posix_basic_descriptor SOURCES ${CURRENT_TEST_SOURCES_DIR}/posix/basic_descriptor.cpp COMPILE_ONLY)
cm_test(NAME asio_test_posix_basic_descriptor_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/posix/basic_descriptor.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_posix_basic_descriptor_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_posix_basic_stream_descriptor SOURCES ${CURRENT_TEST_SOURCES_DIR}/posix/basic_stream_descriptor.cpp COMPILE_ONLY)
cm_test(NAME asio_test_posix_basic_stream_descriptor_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/posix/basic_stream_descriptor.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_posix_basic_stream_descriptor_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_posix_descriptor_base SOURCES ${CURRENT_TEST_SOURCES_DIR}/posix/descriptor_base.cpp COMPILE_ONLY)
cm_test(NAME asio_test_posix_descriptor_base_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/posix/descriptor_base.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_posix_descriptor_base_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_posix_stream_descriptor SOURCES ${CURRENT_TEST_SOURCES_DIR}/posix/stream_descriptor.cpp COMPILE_ONLY)
cm_test(NAME asio_test_posix_stream_descriptor_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/posix/stream_descriptor.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_posix_stream_descriptor_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_posix_stream_descriptor_service SOURCES ${CURRENT_TEST_SOURCES_DIR}/posix/stream_descriptor_service.cpp COMPILE_ONLY)
cm_test(NAME asio_test_posix_stream_descriptor_service_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/posix/stream_descriptor_service.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_posix_stream_descriptor_service_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_raw_socket_service SOURCES ${CURRENT_TEST_SOURCES_DIR}/raw_socket_service.cpp COMPILE_ONLY)
cm_test(NAME asio_test_raw_socket_service_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/raw_socket_service.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_raw_socket_service_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_read SOURCES ${CURRENT_TEST_SOURCES_DIR}/read.cpp)
cm_test(NAME asio_test_read_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/read.cpp)
target_compile_definitions(asio_test_read_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_read_at SOURCES ${CURRENT_TEST_SOURCES_DIR}/read_at.cpp)
cm_test(NAME asio_test_read_at_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/read_at.cpp)
target_compile_definitions(asio_test_read_at_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_read_until SOURCES ${CURRENT_TEST_SOURCES_DIR}/read_until.cpp)
cm_test(NAME asio_test_read_until_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/read_until.cpp)
target_compile_definitions(asio_test_read_until_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_seq_packet_socket_service SOURCES ${CURRENT_TEST_SOURCES_DIR}/seq_packet_socket_service.cpp COMPILE_ONLY)
cm_test(NAME asio_test_seq_packet_socket_service_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/seq_packet_socket_service.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_seq_packet_socket_service_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_signal_set SOURCES ${CURRENT_TEST_SOURCES_DIR}/signal_set.cpp)
cm_test(NAME asio_test_signal_set_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/signal_set.cpp)
target_compile_definitions(asio_test_signal_set_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_signal_set_service SOURCES ${CURRENT_TEST_SOURCES_DIR}/signal_set_service.cpp COMPILE_ONLY)
cm_test(NAME asio_test_signal_set_service_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/signal_set_service.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_signal_set_service_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_socket_acceptor_service SOURCES ${CURRENT_TEST_SOURCES_DIR}/socket_acceptor_service.cpp COMPILE_ONLY)
cm_test(NAME asio_test_socket_acceptor_service_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/socket_acceptor_service.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_socket_acceptor_service_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_socket_base SOURCES ${CURRENT_TEST_SOURCES_DIR}/socket_base.cpp)
cm_test(NAME asio_test_socket_base_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/socket_base.cpp)
target_compile_definitions(asio_test_socket_base_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_steady_timer SOURCES ${CURRENT_TEST_SOURCES_DIR}/steady_timer.cpp COMPILE_ONLY)
cm_test(NAME asio_test_steady_timer_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/steady_timer.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_steady_timer_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_strand SOURCES ${CURRENT_TEST_SOURCES_DIR}/strand.cpp)
cm_test(NAME asio_test_strand_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/strand.cpp)
target_compile_definitions(asio_test_strand_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_stream_socket_service SOURCES ${CURRENT_TEST_SOURCES_DIR}/stream_socket_service.cpp COMPILE_ONLY)
cm_test(NAME asio_test_stream_socket_service_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/stream_socket_service.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_stream_socket_service_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_streambuf SOURCES ${CURRENT_TEST_SOURCES_DIR}/streambuf.cpp)
cm_test(NAME asio_test_streambuf_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/streambuf.cpp)
target_compile_definitions(asio_test_streambuf_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_system_timer SOURCES ${CURRENT_TEST_SOURCES_DIR}/system_timer.cpp COMPILE_ONLY)
cm_test(NAME asio_test_system_timer_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/system_timer.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_system_timer_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_time_traits SOURCES ${CURRENT_TEST_SOURCES_DIR}/time_traits.cpp COMPILE_ONLY)
cm_test(NAME asio_test_time_traits_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/time_traits.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_time_traits_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_wait_traits SOURCES ${CURRENT_TEST_SOURCES_DIR}/wait_traits.cpp COMPILE_ONLY)
cm_test(NAME asio_test_wait_traits_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/wait_traits.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_wait_traits_select PRIVATE ${USE_SELECT})
cm_test(NAME asio_test_waitable_timer_service SOURCES ${CURRENT_TEST_SOURCES_DIR}/waitable_timer_service.cpp COMPILE_ONLY)
cm_test(NAME asio_test_waitable_timer_service_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/waitable_timer_service.cpp COMPILE_ONLY)
target_compile_definitions(asio_test_waitable_timer_service_select PRIVATE ${USE_SELECT})
if(WIN32)
    cm_test(NAME asio_test_windows/basic_handle SOURCES ${CURRENT_TEST_SOURCES_DIR}/windows/basic_handle.cpp COMPILE_ONLY)
    cm_test(NAME asio_test_windows/basic_object_handle SOURCES ${CURRENT_TEST_SOURCES_DIR}/windows/basic_object_handle.cpp COMPILE_ONLY)
    cm_test(NAME asio_test_windows/basic_random_access_handle SOURCES ${CURRENT_TEST_SOURCES_DIR}/windows/basic_random_access_handle.cpp COMPILE_ONLY)
    cm_test(NAME asio_test_windows/basic_stream_handle SOURCES ${CURRENT_TEST_SOURCES_DIR}/windows/basic_stream_handle.cpp COMPILE_ONLY)
    cm_test(NAME asio_test_windows/object_handle SOURCES ${CURRENT_TEST_SOURCES_DIR}/windows/object_handle.cpp COMPILE_ONLY)
    cm_test(NAME asio_test_windows/object_handle_service SOURCES ${CURRENT_TEST_SOURCES_DIR}/windows/object_handle_service.cpp COMPILE_ONLY)
    cm_test(NAME asio_test_windows/overlapped_ptr SOURCES ${CURRENT_TEST_SOURCES_DIR}/windows/overlapped_ptr.cpp COMPILE_ONLY)
    cm_test(NAME asio_test_windows/random_access_handle SOURCES ${CURRENT_TEST_SOURCES_DIR}/windows/random_access_handle.cpp COMPILE_ONLY)
    cm_test(NAME asio_test_windows/random_access_handle_service SOURCES ${CURRENT_TEST_SOURCES_DIR}/windows/random_access_handle_service.cpp COMPILE_ONLY)
    cm_test(NAME asio_test_windows/stream_handle SOURCES ${CURRENT_TEST_SOURCES_DIR}/windows/stream_handle.cpp COMPILE_ONLY)
    cm_test(NAME asio_test_windows/stream_handle_service SOURCES ${CURRENT_TEST_SOURCES_DIR}/windows/stream_handle_service.cpp COMPILE_ONLY)
endif()
cm_test(NAME asio_test_write SOURCES ${CURRENT_TEST_SOURCES_DIR}/write.cpp)
cm_test(NAME asio_test_write_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/write.cpp)
cm_test(NAME asio_test_write_at SOURCES ${CURRENT_TEST_SOURCES_DIR}/write_at.cpp)
cm_test(NAME asio_test_write_at_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/write_at.cpp)

if(OpenSSL_FOUND)
    cm_test(NAME asio_test_asio_test_basic_context SOURCES ${CURRENT_TEST_SOURCES_DIR}/ssl/basic_context.cpp COMPILE_ONLY)
    cm_test(NAME asio_test_asio_test_basic_context_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/ssl/basic_context.cpp COMPILE_ONLY)
    target_compile_definitions(asio_test_asio_test_basic_context_select PRIVATE ${USE_SELECT_SSL})
        
    cm_test(NAME asio_test_asio_test_context_base SOURCES ${CURRENT_TEST_SOURCES_DIR}/ssl/context_base.cpp COMPILE_ONLY)
    cm_test(NAME asio_test_asio_test_context_base_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/ssl/context_base.cpp COMPILE_ONLY)
    target_compile_definitions(asio_test_asio_test_context_base_select PRIVATE ${USE_SELECT_SSL})
        
    cm_test(NAME asio_test_asio_test_context_service SOURCES ${CURRENT_TEST_SOURCES_DIR}/ssl/context_service.cpp COMPILE_ONLY)
    cm_test(NAME asio_test_asio_test_context_service_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/ssl/context_service.cpp COMPILE_ONLY)
    target_compile_definitions(asio_test_asio_test_context_service_select PRIVATE ${USE_SELECT_SSL})
        
    cm_test(NAME asio_test_asio_test_context SOURCES ${CURRENT_TEST_SOURCES_DIR}/ssl/context.cpp COMPILE_ONLY)
    cm_test(NAME asio_test_asio_test_context_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/ssl/context.cpp COMPILE_ONLY)
    target_compile_definitions(asio_test_asio_test_context_select PRIVATE ${USE_SELECT_SSL})
        
    cm_test(NAME asio_test_asio_test_rfc2818_verification SOURCES ${CURRENT_TEST_SOURCES_DIR}/ssl/rfc2818_verification.cpp COMPILE_ONLY)
    cm_test(NAME asio_test_asio_test_rfc2818_verification_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/ssl/rfc2818_verification.cpp COMPILE_ONLY)
    target_compile_definitions(asio_test_asio_test_rfc2818_verification_select PRIVATE ${USE_SELECT_SSL})

    cm_test(NAME asio_test_asio_test_stream_base SOURCES ${CURRENT_TEST_SOURCES_DIR}/ssl/stream_base.cpp COMPILE_ONLY)
    cm_test(NAME asio_test_asio_test_stream_base_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/ssl/stream_base.cpp COMPILE_ONLY)
    target_compile_definitions(asio_test_asio_test_stream_base_select PRIVATE ${USE_SELECT_SSL})

    cm_test(NAME asio_test_asio_test_stream_service SOURCES ${CURRENT_TEST_SOURCES_DIR}/ssl/stream_service.cpp COMPILE_ONLY)
    cm_test(NAME asio_test_asio_test_stream_service_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/ssl/stream_service.cpp COMPILE_ONLY)
    target_compile_definitions(asio_test_asio_test_stream_service_select PRIVATE ${USE_SELECT_SSL})

    cm_test(NAME asio_test_asio_test_stream SOURCES ${CURRENT_TEST_SOURCES_DIR}/ssl/stream.cpp COMPILE_ONLY)
    cm_test(NAME asio_test_asio_test_stream_select SOURCES ${CURRENT_TEST_SOURCES_DIR}/ssl/stream.cpp COMPILE_ONLY)
    target_compile_definitions(asio_test_asio_test_stream_select PRIVATE ${USE_SELECT_SSL})

endif()
