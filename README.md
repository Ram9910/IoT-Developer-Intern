class SmartAntiTheftSystem:
    def __init__(self):
        self.armed = False
        self.intrusion_detected = False

    def arm_system(self):
        self.armed = True
        print("System armed.")

    def disarm_system(self):
        self.armed = False
        print("System disarmed.")

    def detect_intrusion(self):
        if self.armed:
            self.intrusion_detected = True
            print("Intrusion detected! Alerting authorities.")
        else:
            print("System not armed. Intrusion detection inactive.")

# Usage example
if __name__ == "__main__":
    anti_theft_system = SmartAntiTheftSystem()
    anti_theft_system.detect_intrusion()  # System not armed. Intrusion detection inactive.
    anti_theft_system.arm_system()  # System armed.
    anti_theft_system.detect_intrusion()  # Intrusion detected! Alerting authorities.
    anti_theft_system.disarm_system()  # System disarmed.
    anti_theft_system.detect_intrusion()  # System not armed. Intrusion detection inactive.
