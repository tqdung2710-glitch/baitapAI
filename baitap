import folium
from folium import plugins

ueh_coords = [10.773408143015685, 106.67751756472136]
m = folium.Map(location=ueh_coords, zoom_start=16, control_scale=True)

fg_ueh = folium.FeatureGroup(name='Đai học (UEH)')
fg_public = folium.FeatureGroup(name='Địa điểm công cộng')

folium.Marker(
    location=ueh_coords,
    popup='<b>UEH - Cơ sở C</b><br>Đại học Kinh tế TP. Hồ Chí Minh',
    icon=folium.Icon(color='red', icon='university', prefix='fa')
).add_to(fg_ueh)

public_places = [
    {"name": " Học viện Hành chính và Quản trị công", "coords": [10.773788895029023, 106.67634228889187], "desc": "Trường học."},
    {"name": "Hệ thống trường PennSchool", "coords": [10.773123463768941, 106.67540060540381], "desc": "Trường học."},
    {"name": "Centerphones", "coords": [10.772589049574822, 106.67610428158727], "desc": "Cửa hàng."},
    {"name": "Nhà hát Hòa Bình", "coords": [10.772352464169874, 106.67406767701074], "desc": "Nhà hát."},
    {"name": "Việt Nam Quốc Tự", "coords": [10.772148618487902, 106.6734993011157], "desc": "Chùa."}
]

for place in public_places:
    folium.Marker(
        location=place["coords"],
        popup=f"<b>{place['name']}</b><br>{place['desc']}",
        icon=folium.Icon(color='blue', icon='info-sign')
    ).add_to(fg_public)

fg_ueh.add_to(m)
fg_public.add_to(m)

folium.LayerControl().add_to(m)

m.save('ban_do_tuong_tac_UEH.html')

print("Đã tạo bản đồ thành công! Hãy mở file 'ban_do_tuong_tac_UEH.html' để xem.")
