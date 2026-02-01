document.getElementById("calc").addEventListener("click", function () {
    const money = parseInt(document.getElementById("money").value);

    // CHIA THEO % ĐỂ KHÔNG BAO GIỜ BỊ LẺ
    const plan = {
        giaDinh: money * 0.30,
        quaBieu: money * 0.20,
        liXi: money * 0.20,
        trangPhuc: money * 0.10,
        anUong: money * 0.10,
        hocTap: money * 0.05,
        duPhong: money * 0.05
    };

    // LÀM TRÒN ĐẸP — về 1.000đ
    for (let i in plan) {
        plan[i] = Math.round(plan[i] / 1000) * 1000;
    }

    // HIỂN THỊ
    document.getElementById("p1").innerText = plan.giaDinh.toLocaleString() + "đ";
    document.getElementById("p2").innerText = plan.quaBieu.toLocaleString() + "đ";
    document.getElementById("p3").innerText = plan.liXi.toLocaleString() + "đ";
    document.getElementById("p4").innerText = plan.trangPhuc.toLocaleString() + "đ";
    document.getElementById("p5").innerText = plan.anUong.toLocaleString() + "đ";
    document.getElementById("p6").innerText = plan.hocTap.toLocaleString() + "đ";
    document.getElementById("p7").innerText = plan.duPhong.toLocaleString() + "đ";
});
