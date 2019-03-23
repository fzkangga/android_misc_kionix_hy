# android_misc_kionix_hy

implement to dts for g151 a.k.a Andromax A16C3H

	&soc {
		i2c@78b5000 { /* BLSP1 QUP1 */
			kionix@e {
				compatible = "kionix,kxtj2-1009";
				reg = <0x0e>;
				interrupt-parent = <&msm_gpio>;
				interrupts = <96 0x2002>;
				vdd-supply = <&pm8909_l17>;
				vio-supply = <&pm8909_l6>;
				kionix,min_interval = <5>;
				kionix,poll_interval = <100>;
				kionix,accel_direction = <2>;
				kionix,accel_irq_use_drdy = <0>;
				kionix,accel_res = <12>;
				kionix,accel_g_range = <2>;
			};
		};
	};

implement to dts for Andromax G36C1H

	&i2c_0 { /* BLSP1 QUP2 */
		kionix@e {
			compatible = "kionix,kxtj2-1009";
			reg = <0x0e>;
			interrupt-parent = <&msm_gpio>;
			interrupts = <112 0x2002>;
			vdd-supply = <&pm8916_l17>;
			vio-supply = <&pm8916_l6>;
			kionix,min_interval = <5>;
			kionix,poll_interval = <100>;
			kionix,accel_direction = <2>;
			kionix,accel_irq_use_drdy = <0>;
			kionix,accel_res = <12>;
			kionix,accel_g_range = <2>;
		};
	};
